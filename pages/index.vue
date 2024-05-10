<template>
    <div class="mt-5 mx-auto max-w-7xl px-6 lg:px-8">
        <div class="mx-auto max-w-2xl text-center">
            <h1 class="text-4xl font-bold tracking-tight text-gray-900 sm:text-6xl">An Alcove of Literary History</h1>
            <p class="mt-6 text-lg leading-8 text-gray-600">Anim aute id magna aliqua ad ad non deserunt
                sunt. Qui irure qui lorem cupidatat commodo. Elit sunt amet fugiat veniam occaecat fugiat
                aliqua.</p>
            <div class="mt-10 flex items-center justify-center gap-x-6">
                <a href="#" class="w-36 rounded-3xl bg-slate-700 px-3.5 py-2.5 text-sm font-semibold text-white shadow-sm hover:bg-slate-900 focus-visible:outline focus-visible:outline-2 focus-visible:outline-offset-2 focus-visible:outline-indigo-600">Start Reading</a>
                <a href="#" class="text-sm font-semibold leading-6 text-gray-900">Upload Story <span
                        aria-hidden="true">→</span></a>
            </div>
        </div>
        <div class="mt-16 flow-root sm:mt-24">
            <div class="-m-2 p-2 lg:-m-4 lg:p-4">
                <img src="public/images/picture1.jpg" alt="" width="2211" height="1221" class="rounded-md shadow-2xl ring-1 ring-gray-900/10" />
            </div>
        </div>
    </div>
    <div class="mx-auto mt-28 mb-10 max-w-7xl px-6 sm:mt-32 lg:px-8">
                <div class="mx-auto max-w-xl lg:text-center">
                    <h2 class="text-base font-semibold leading-7 text-slate-700">Uncover Forgotten Gems</h2>
                    <p class="mt-2 text-2xl font-bold tracking-tight text-gray-900 sm:text-4xl">Your Destination for Literary Finds</p>
                    <p class="mt-6 text-lg leading-8 text-gray-600">Where every book tells a story that brings nostalgia in every aisle.</p>
                </div>
                <div class="mx-auto mt-16 max-w-2xl sm:mt-20 lg:mt-24 lg:max-w-4xl">
                    <dl class="grid max-w-xl grid-cols-1 gap-x-8 gap-y-10 lg:max-w-none lg:grid-cols-2 lg:gap-y-16">
                        <div v-for="feature in features" :key="feature.name" class="relative pl-16">
                            <dt class="text-base font-semibold leading-7 text-gray-900">
                                <div
                                    class="absolute left-0 top-0 flex h-10 w-10 items-center justify-center rounded-lg bg-slate-700">
                                    <component :is="feature.icon" class="h-6 w-6 text-white" aria-hidden="true" />
                                </div>
                                {{ feature.name }}
                            </dt>
                            <dd class="mt-2 text-base leading-7 text-gray-600">{{ feature.description }}</dd>
                        </div>
                    </dl>
                </div>
            </div>
</template>
<script setup>
import { ref } from 'vue'
import {
    BookOpenIcon,
} from '@heroicons/vue/24/outline'
import { CheckIcon } from '@heroicons/vue/20/solid'

    const features = [
    {
        name: 'Alamat',
        description:
            'Morbi viverra dui mi arcu sed. Tellus semper adipiscing suspendisse semper morbi. Odio urna massa nunc massa.',
        icon: BookOpenIcon,
    },
    {
        name: 'Epiko',
        description:
            'Sit quis amet rutrum tellus ullamcorper ultricies libero dolor eget. Sem sodales gravida quam turpis enim lacus amet.',
        icon: BookOpenIcon,
    },
    {
        name: 'Kasaysayan',
        description:
            'Quisque est vel vulputate cursus. Risus proin diam nunc commodo. Lobortis auctor congue commodo diam neque.',
        icon: BookOpenIcon,
    },
    {
        name: 'Kwentong Bayan',
        description:
            'Arcu egestas dolor vel iaculis in ipsum mauris. Tincidunt mattis aliquet hac quis. Id hac maecenas ac donec pharetra eget.',
        icon: BookOpenIcon,
    },
    {
        name: 'Maikling Kwento',
        description:
            'Morbi viverra dui mi arcu sed. Tellus semper adipiscing suspendisse semper morbi. Odio urna massa nunc massa.',
        icon: BookOpenIcon,
    },
    {
        name: 'Nobela',
        description:
            'Sit quis amet rutrum tellus ullamcorper ultricies libero dolor eget. Sem sodales gravida quam turpis enim lacus amet.',
        icon: BookOpenIcon,
    },
    {
        name: 'Sawikan',
        description:
            'Quisque est vel vulputate cursus. Risus proin diam nunc commodo. Lobortis auctor congue commodo diam neque.',
        icon: BookOpenIcon,
    },
    {
        name: 'Tula',
        description:
            'Arcu egestas dolor vel iaculis in ipsum mauris. Tincidunt mattis aliquet hac quis. Id hac maecenas ac donec pharetra eget.',
        icon: BookOpenIcon,
    },
  
]
</script>

