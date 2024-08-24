<template>
    <Head title="Products"/>
    <FrontendLayout>
        <div class="mt-4 mx-4 ">
            <div class="flex justify-between">
                <h5>Product Lists</h5>
                <Link href="route('product.create')" class="bg-blue-500 text-white p-3 rounded mb-4">Add Product</Link>
                    <table>
                        <thead>
                            <tr class="w-full bg-white border border-grey-200 shadow">
                                <th class="py-2 px-4 text-left border">Id</th>
                                <th class="py-2 px-4 text-left border">name</th>
                                <th class="py-2 px-4 text-left border">price</th>
                                <th class="py-2 px-4 text-left border">action</th>
                                <th class="py-2 px-4 text-left border">Id</th>
                            </tr>
                        </thead>
                    </table>
            </div>
        </div>
    </FrontendLayout>
</template>

<script setup>
import FrontendLayout from '@/layouts/FrontendLayout.vue';
import { Head } from '@inertiajs/vue3';
</script>
