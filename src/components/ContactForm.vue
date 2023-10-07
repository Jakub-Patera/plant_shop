<template>
    <div class=" bg-blue-800 h-80 w-80 " >

        <form @submit.prevent="submitForm">
            <label for="name">Name:</label>
            <input type="text" id="name" v-model="name" required class="bg-red-500">
            <label for="email">Email:</label>
            <input type="email" id="email" v-model="email" required>
            <label for="message">Message:</label>
            <textarea id="message" v-model="message" required></textarea>
            <button type="submit">Submit</button>
        </form>
    </div>



    <!-- footer info -->

    
        <div class="flex flex-wrap justify-between items-center">
            <!-- Logo and email subscriber -->
            <div class="w-full md:w-1/4 flex justify-center items-center">
                <div class="flex flex-col items-center">
                    <img src="/path/to/logo.png" alt="Logo" class="w-24 h-24 mb-4">
                    <form @submit.prevent="subscribe">
                        <label for="email" class="sr-only">Email address</label>
                        <div class="flex items-center">
                            <input type="email" id="email" v-model="email" required class="rounded-l-lg px-4 py-2 w-64 border-t mr-0 border-b border-l text-gray-800 border-gray-200 bg-white">
                            <button type="submit" class="px-8 rounded-r-lg bg-blue-500 text-white font-bold p-4 uppercase border-blue-500 border-t border-b border-r">Subscribe</button>
                        </div>
                    </form>
                </div>
            </div>
            </div>

            <!-- Address -->
      
    </template>

    <!-- <script>
    export default {
        data() {
            return {
                email: ''
            }
        },
        methods: {
            subscribe() {
                // Handle email subscription here
                console.log('Email subscribed:', this.email)
            }
        }
    }
    </script> -->


<script>
export default {
    data() {
        return {
            name: '',
            email: '',
            message: ''
        }
    },
    methods: {
        submitForm() {
            // Handle form submission here
            console.log('Form submitted!')
        }
    }
}
</script>
