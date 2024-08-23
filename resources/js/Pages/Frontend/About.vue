
    <template>
        <Frontend>
            <Head title="About Us"/>
            <h2>This is a {{title}}</h2>
        </Frontend>
    </template>

    <script setup>
     import Frontend from '@/Layouts/FrontendLayout.vue';
     import { Head } from '@inertiajs/vue3';
        defineProps({
            title: String
        });
    </script>
