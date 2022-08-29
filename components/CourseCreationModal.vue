




















<script setup>


</script>

<template>
    <div class="modal-overlay" @click="$emit('close-modal')">
        <div class="modal" @click.stop>

            <div class="header">
                <h2>Add course information</h2>
            </div>

            <div class="body">
                <form @submit.prevent>

                    <div class="courseName">
                        <label>Course Name:</label>
                        <input v-model.trim="courseName" name="courseName" type="text" required
                            placeholder="Enter course name">
                        <p>Name: {{ courseName }}</p>
                    </div>
                    <div class="description">
                        <label>Description:</label>
                        <input v-model.trim="description" name="description" type="text"
                            placeholder="Enter description">
                    </div>
                    <div class="lessons">
                        <label>Lessons(count):</label>
                        <input v-model.number="lessons" name="lessons" type="number" required
                            placeholder="Enter count of lessons">
                            <p>Lessons: {{lessons}}</p>
                    </div>
                    <div class="image">
                        <label>Image URL:</label>
                        <input v-model.trim="image" name="image" type="text" placeholder="Enter image URL">
                    </div>
                    <button type="submit" v-if="courseName && lessons" @click="$emit('close-modal')">Submit</button>
                    <button type="submit" v-else>Submit</button>
                </form>
            </div>

            <div class="footer">
            </div>

        </div>
    </div>
</template>

<style scoped>
.modal-overlay {
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    display: flex;
    justify-content: center;
    background-color: #706d6dda;
}

.modal {
    text-align: center;
    background-color: bisque;
    height: 70vh;
    width: 500px;
    margin-top: 10%;
    border-radius: 20px;
}

.header {
    border-bottom: solid 3px black;
    margin-bottom: 30px;
}

.courseName,
.description,
.lessons,
.image {
    display: flex;
    justify-content: center;
    align-items: center;
}

label {
    margin-top: 10px;
    margin-bottom: 10px;
}

input {
    height: 3vh;
}
</style>