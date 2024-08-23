
    <template>
        <div>
            <h2>This is a {{title}}</h2>
        </div>
    </template>

    <script setup>
        defineProps({
            title: String
        });
    </script>
