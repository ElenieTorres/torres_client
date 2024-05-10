<template>
    <div class="bg-white">
        <div class="mx-auto max-w-2xl px-8 py-16 sm:px-6 sm:py-10 lg:grid lg:max-w-7xl lg:grid-cols-2 lg:gap-x-8 lg:px-8">
            <!-- Book details -->
            <div class="lg:max-w-lg lg:self-end">
                <nav aria-label="Breadcrumb">
                    <ol role="list" class="flex items-center space-x-2">
                        <li v-for="(breadcrumb, breadcrumbIdx) in book.breadcrumbs" :key="breadcrumb.id">
                            <div class="flex items-center text-sm">
                                <a :href="breadcrumb.href" class="font-medium text-gray-500 hover:text-gray-900">{{
                                    breadcrumb.name }}</a>
                                <svg v-if="breadcrumbIdx !== book.breadcrumbs.length - 1" viewBox="0 0 20 20"
                                    fill="currentColor" aria-hidden="true" class="ml-2 h-5 w-5 flex-shrink-0 text-gray-300">
                                    <path d="M5.555 17.776l8-16 .894.448-8 16-.894-.448z" />
                                </svg>
                            </div>
                        </li>
                    </ol>
                </nav>

                <h1 class="mt-4 text-3xl font-bold tracking-tight text-gray-900 sm:text-4xl">{{ book.title }}</h1>
                <p class="mt-4 italic text-gray-500">{{ book.author }}</p>

                <section aria-labelledby="information-heading" class="mt-4">

                    <div class="flex items-center">
                       
                        <h2 class="sr-only">Reviews</h2>
                        <div class="flex items-center">
                            <div>
                                <div class="flex items-center">
                                    <StarIcon v-for="rating in [0, 1, 2, 3, 4]" :key="rating"
                                        :class="[reviews.average > rating ? 'text-yellow-400' : 'text-gray-300', 'h-5 w-5 flex-shrink-0']"
                                        aria-hidden="true" />
                                </div>
                                <p class="sr-only">{{ reviews.average }} out of 5 stars</p>
                            </div>
                            <p class="ml-2 text-sm text-gray-500">{{ reviews.totalCount }} reviews</p>
                        </div>
                        
                    </div>

                    <div class="mt-4 space-y-6">
                        <p class="text-base text-gray-500">{{ book.description }}</p>
                    </div>

                 
                </section>
            </div>

            <!-- Book image -->
            <div class="mt-10 lg:col-start-2 lg:row-span-2 lg:mt-0 lg:self-center">
                <div class="aspect-h-1 aspect-w-1 lg:ml-24 sm:ml-0  overflow-hidden rounded-lg">
                    <img :src="book.imageSrc" :alt="book.imageAlt" class="h-full w-full object-cover object-center" />
                </div>
            </div>

            <!-- Book form -->
            <div class="mt-10 lg:col-start-1 lg:row-start-2 lg:max-w-lg lg:self-start">
                <form>
                    <div>
                        <button type="submit"
                            class="flex w-full items-center justify-center rounded-3xl border border-transparent bg-slate-950 px-8 py-3 text-base font-medium text-white hover:bg-slate-700 focus:outline-none focus:ring-2 focus:ring-indigo-500 focus:ring-offset-2 focus:ring-offset-gray-50">READ NOW</button>
                    </div>
                </form>
            </div>
        </div>
    </div>
</template>
  
<script setup>
import { ref } from 'vue'
import { CheckIcon, QuestionMarkCircleIcon, StarIcon } from '@heroicons/vue/20/solid'
import { RadioGroup, RadioGroupDescription, RadioGroupLabel, RadioGroupOption } from '@headlessui/vue'
import { ShieldCheckIcon } from '@heroicons/vue/24/outline'

const book = {
    title: 'TUWAANG AT ANG DILAG NG KALANGITAN NG BUHONG',
    author: 'by E. ARSENIO MANUEL',
    href: '#',
    description: "The story about the adventure of the legendary hero Tuwaang in rescuing a distressed maiden, which came from the sky, from a ferocious giant suitor whom she declined.",
    imageSrc: '/images/book4.jpg',
    imageAlt: '',
    breadcrumbs: [
        { id: 1, name: 'Epiko', href: '#' },
        { id: 2, name: 'Cultura', href: '#' },
    ],
}
const reviews = { average: 5, totalCount: 1624 }
</script>