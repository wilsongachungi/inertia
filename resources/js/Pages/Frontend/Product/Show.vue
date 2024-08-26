<template>

    <Head title="Show Product" />
    <FrontendLayout>
        <div class="mt-4 mx-4 ">
            <div class="flex justify-between">
                <h5>Show Product</h5>
                <Link :href="route('product.index')"
                    class="bg-red-500 text-white p-3 rounded py-2 px-5  mb-4 inline-block">Back</Link>
            </div>

                <div class="grid grid-cols-12 gap-4">
                    <div class="col-span-6">
                        <div class="mb-3">
                            <label for="">Product Name</label>
                            <p> {{ product.name }} </p>
                        </div>
                        <div class="mb-3">
                            <label for="">Product Price</label>
                            <p> {{ product.price }} </p>
                        </div>
                    </div>
                </div>
        </div>
    </FrontendLayout>
</template>

<script setup>
import FrontendLayout from '@/layouts/FrontendLayout.vue';
import { Head, Link, useForm } from '@inertiajs/vue3';

const props = defineProps({
    errors: Object,
    product: Object,
});

</script>
