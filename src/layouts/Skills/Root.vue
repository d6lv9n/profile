<template>
    <div class="flex flex-col gap-y-6 my-6 w-full
    sm:flex-row sm:gap-y-0 sm:justify-between">
        <div class="rounded-lg select-none
        lg:max-w-sm">
            <div>
                <span class="border-b-2 border-white pb-1.5 pr-6
                sm:border-gray-400 sm:px-3">
                    <span class="font-bold text-lg
                    sm:text-2xl">Hard skills</span>
                </span>
            </div>

            <ul
            role="list"
            class="flex flex-grow flex-row flex-shrink flex-wrap gap-3 pt-6">
                <li
                v-for="skill in hardSkills"
                :key="skill"
                class="border border-blue-400 flex-shrink-0 font-semibold px-3 py-1.5 rounded-full text-blue-400">{{ skill }}</li>
            </ul>
        </div>

        <div class="rounded-lg select-none
        lg:max-w-sm">
            <div>
                <span class="border-b-2 border-white pb-1.5 pr-6
                sm:border-gray-400 sm:px-3">
                    <span class="font-bold text-lg
                    sm:text-2xl">Soft skills</span>
                </span>
            </div>

            <ul
            role="list"
            class="flex flex-grow flex-row flex-shrink flex-wrap gap-3 pt-6">
                <li
                v-for="skill in softSkills"
                :key="skill"
                class="border border-green-400 flex-shrink-0 font-semibold px-3 py-1.5 rounded-full text-green-400">{{ skill }}</li>
            </ul>
        </div>
    </div>
</template>

<script setup>
// Data
const hardSkills = [
    'HTML',
    'CSS',
    'Tailwind CSS',
    'JavaScript',
    'ES6',
    'jQuery',
    'Axios',
    'Vue (Vue.js)',
    'Vue Composition API',
    'Vuex',
    'Vue Meta',
    'Vue Router',
    'Vue I18n',
    'PHP',
    'Laravel',
    'MySQL',
    'PostgreSQL',
    'Schema Design',
    'Database Design',
    'Debugging',
    'Responsive Design',
    'Code Review',
    'Code Refactoring',
    'Performance Optimization',
    'SEO Best Practices',
    'Clean Code Principles',
    'Single Page Application (SPA)',
    'Content Management Systems (CMS)',
    'Content Relational Management (CRM)',
    'FFmpeg Integration',
    'Media Processing',
    'Queue Processing',
    'RESTful Web Services',
    'Creating Error Logging System',
    'Creating Error Notification System',
    'API Development',
    'Authentication Tracking',
    'RESTful API',
    'REST API Design',
    'Service Patterns Architecture',
    'Best Practices Lover',
    'Clean Code Mania',
    'Security Best Practices',
    'Software Development Life Cycle (SDLC)',
    'Object-Oriented Programming (OOP)',
    'Model-View-Controller (MVC)',
];
const softSkills = [
    'Resilience',
    'Long-term Thinking',
    'Analytical Thinking',
    'Decision Making',
    'Problem Solving',
    'Open-mindedness',
    'Adaptability',
    'Deep Thinker',
    'Attention to Detail',
    'Energetic',
    'Empathy',
    'Ambitious',
    'Self-Motivation',
    'Continuous Learning',
    'Positive Attitude',
    'Emotional Intelligence',
    'Critical Thinking',
    'Independent and Team Player',
];
// const weaknesses = [
//     'Perfectionism',
//     'Overthinking',
//     'Sensitive',
//     'Cautious',
//     'Procrastination',
//     'Difficulty Saying No',
//     'Fear of Failure',
//     'Difficulty Delegating',
//     'Impatience',
//     'Overcommitting',
//     'Difficulty with Public Speaking',
//     'Shy',
// ];
</script>
