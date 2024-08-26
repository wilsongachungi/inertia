<template>
    <Head title="Products"/>
    <FrontendLayout>
        <div v-if="$page.props.flash.message" class="alert bg-green-200 mt-4 mx-5 px-4 py-2">
            {{ $page.props.flash.message }}
          </div>
        <div class="mt-4 mx-4 ">
            <div class="flex justify-between">
                <h5>Product Lists</h5>
                <Link :href="route('product.create')" class="bg-blue-500 text-white p-3 rounded mb-4">Add Product</Link>
            </div>
                    <table class="w-full bg-white border border-grey-200 shadow">
                        <thead>
                            <tr >
                                <th class="py-2 px-4 text-left border">Id</th>
                                <th class="py-2 px-4 text-left border">name</th>
                                <th class="py-2 px-4 text-left border">price</th>
                                <th class="py-2 px-4 text-left border">action</th>
                            </tr>
                        </thead>
                        <tbody>
                            <tr
                            v-for="(item, index) in products"
                            :key="index"
                            >
                                <td class="py-2 px-4 border">{{ item.id }}</td>
                                <td class="py-2 px-4 border">{{ item.name }}</td>
                                <td class="py-2 px-4 border">{{ item.price }}</td>
                                <td>
                                    <Link :href="route('product.show', item.id)" class="px-2 py-1 text-sm bg-blue-300 text-dark me-2  rounded inline-block">Show</Link>
                                    <Link :href="route('product.edit', item.id)" class="px-2 py-1 bg-green-500 text-white me-2  rounded inline-block">Edit</Link>
                                    <button type="submit" class="px-2 py-1 bg-red-500 text-white me-2  rounded inline-block">Delete</button>
                                </td>
                            </tr>
                        </tbody>
                    </table>
        </div>
    </FrontendLayout>
</template>

<script setup>
import FrontendLayout from '@/layouts/FrontendLayout.vue';
import { Head, Link } from '@inertiajs/vue3';

defineProps({
    products: Array
})
</script>
