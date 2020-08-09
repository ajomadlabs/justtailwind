<template>
    <center>
        <!-- MAIN SECTION -->
        <div
            style="max-width: 1132px"
        >
            <!-- CONTENT SECTION -->
            <div
                class="flex items-start justify-between"
            >
                <!-- PROFILE SECTION -->
                <div
                    class="w-7/12"
                >
                    <!-- FIRST SECTION -->
                    <div
                        class="flex items-start pb-22625 border-b-2 border-solid border-just-tailwind-gray-300"
                    >
                        <!-- PROFILE IMAGE -->
                        <div
                            class="w-5150 h-5150"                        
                        >
                            <img
                                src="@/assets/images/profile3x.png"
                                alt="Profile Image"
                                class="object-cover h-full w-full"
                            />
                        </div>
                        <!-- END -->

                        <!-- CONTENT SECTION -->
                        <div
                            class="ml-21375"
                        >
                            <!-- NAME SECTION -->
                            <div>
                                <h1
                                    class="leading-normal tracking-normal text-left font-bold text-39 text-just-tailwind-black-900"
                                >
                                    {{ name }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- PROFESSION SECTION -->
                            <div
                                class="mt-0275"
                            >
                                <p
                                    class="leading-normal tracking-normal text-left font-normal text-16 text-just-tailwind-gray-700"
                                >
                                    {{ profession }}
                                </p>
                            </div>
                            <!-- END -->

                            <!-- AMOUNT SECTION -->
                            <div
                                class="mt-0525"
                            >
                                <p
                                    class="leading-normal tracking-normal text-left font-normal text-16 text-just-tailwind-gray-700"
                                >
                                    <span class="font-bold text-just-tailwind-black">${{ amount }}</span> / Session
                                </p>
                            </div>
                            <!-- END -->

                            <!-- TAG SECTION -->
                            <div
                                class="mt-11875 flex flex-wrap"
                            >
                                <div
                                    v-for="(tag,i) in tags"
                                    :key="i"
                                    class="px-2 py-2 rounded"
                                    style="background-color: rgba(179, 189, 201, 0.23);"
                                    :class="i == 0 ? 'ml-0' : 'ml-4'"
                                >
                                    <p
                                        class="leading-normal tracking-normal text-center text-16 font-bold text-just-tailwind-black"
                                    >
                                        {{ tag.name }}
                                    </p>
                                </div>
                            </div>
                            <!-- END -->
                        </div>
                        <!-- END -->
                    </div>
                    <!-- END -->
                    <!-- SECOND SECTION -->
                    <div
                        class="mt-12 pb-22625 border-b-2 border-solid border-just-tailwind-gray-300"
                    >
                        <!-- CONTENT SECTION -->
                        <div
                            v-for="(info, i) in information"
                            :key="i"
                            :class="i == 0 ? 'mt-0' : 'mt-8'"
                        >
                            <div
                                class="flex items-center"
                            >

                                <!-- ICON SECTION -->
                                <div
                                    style="background-color: rgba(0, 123, 254, 0.2);"
                                    class="w-12 h-12 rounded-full"
                                >
                                    <img
                                        :src="getImages(info.img)"
                                        class="py-2"
                                        alt="mask"
                                    />
                                </div>
                                <!-- END -->

                                <!-- TEXT SECTION -->
                                <div
                                    class="text-left ml-4"
                                >
                                    <p
                                        class="text-left leading-normal tracking-normal text-20 text-just-tailwind-gray-700 font-semibold"
                                    >
                                       {{ info.desc }}
                                    </p>
                                </div>
                                <!-- END -->

                            </div>
                        </div>
                        <!-- END -->
                        <!-- QUOTE SECTION -->
                        <div
                            class="mt-12"
                        >
                            <!-- FIRST SECTION -->
                            <div
                                class="text-left"
                            >
                                <img
                                    src="@/assets/images/opening-quote.svg"
                                    alt="quote"
                                />
                            </div>
                            <!-- END -->

                            <!-- SECOND SECTION -->
                            <div
                                class="my-035 ml-11875"
                            >
                                <p
                                    class="text-left leading-normal tracking-normal text-just-tailwind-black text-31 font-normal"
                                    v-html="quote"
                                />
                            </div>
                            <!-- END -->

                            <!-- THIRD SECTION -->
                            <div
                                class="flex w-full justify-end"
                            >
                                <img
                                    src="@/assets/images/closing-quote.svg"
                                    alt="quote"
                                />
                            </div>
                            <!-- END -->
                        </div>
                        <!-- END -->
                    </div>
                    <!-- END -->
                    <!-- THIRD SECTION -->
                    <div
                        class="pb-22625 border-b-2 border-solid border-just-tailwind-gray-300"
                    >
                        <!-- HEADER SECTION -->
                        <div
                            class="my-20"
                        >
                            <h3
                                class="text-39 text-left leading-normal tracking-normal font-bold text-just-tailwind-black-900"
                            >
                                More about me
                            </h3>
                        </div>
                        <!-- END -->
                        <!-- CONTENT SECTION -->
                        <div
                            v-for="(data, i) in aboutMe"
                            :key="i"
                        >
                            <!-- HEADER SECTION -->
                            <div>
                                <h1
                                    class="text-25 text-left leading-normal tracking-normal text-just-tailwind-black-900 font-bold"
                                >
                                    {{ data.title }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- DESCRIPTION -->
                            <div
                                class="mt-8 mb-16"
                            >
                                <p
                                    class="text-20 font-normal text-left leading-normal tracking-normal text-just-tailwind-black"
                                >
                                    {{ data.desc }}
                                </p>
                            </div>
                            <!-- END -->
                        </div>
                        <!-- END -->
                    </div>
                    <!-- END -->
                    <!-- FOURTH SECTION -->
                    <div>
                        <!-- HEADER SECTION -->
                        <div
                            class="my-20"
                        >
                            <h3
                                class="text-39 text-left leading-normal tracking-normal font-bold text-just-tailwind-black-900"
                            >
                                Reviews
                            </h3>
                        </div>
                        <!-- END -->
                        <!-- CONTENT SECTION -->
                        <div
                            v-for="(data, i) in reviews"
                            :key="i"
                        >
                            <!-- HEADER SECTION -->
                            <div
                                class="flex items-center"
                            >
                                <div
                                    class="w-12 h-12"
                                >
                                    <img
                                        :src="getImages(data.img)"
                                        :alt="data.name"
                                        class="h-full w-full object-contain"
                                    />
                                </div>
                                <h1
                                    class="ml-8 text-25 text-left leading-normal tracking-normal text-just-tailwind-black-900 font-bold"
                                >
                                    {{ data.name }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- DESCRIPTION -->
                            <div
                                class="mt-8 mb-16"
                            >
                                <p
                                    class="text-20 font-normal text-left leading-normal tracking-normal text-just-tailwind-black"
                                >
                                    {{ data.desc }}
                                </p>
                            </div>
                            <!-- END -->
                        </div>
                        <!-- END -->

                    </div>
                    <!-- END -->
                </div>
                <!-- END -->

                <!-- SLOT SECTION -->
                <div
                    class="w-843125 border border-solid border-just-tailwind-gray bg-just-tailwind-white rounded-12 py-6 px-104375 shadow-slot"
                >
                    <!-- AMOUNT SECTION -->
                    <div>
                        <p
                            class="leading-normal tracking-normal text-left font-normal text-16 text-just-tailwind-gray-700"
                        >
                            <span class="font-bold text-just-tailwind-black">${{ amount }}</span> / Session
                        </p>
                    </div>
                    <!-- END -->

                    <!-- TIME SECTION -->
                    <div
                        class="text-left"
                    >
                        <div
                            class="mt-0625 px-043 w-1875 py-043 text-center border-2 border-solid border-just-tailwind-black rounded-lg"
                            style="background-color:rgba(179, 189, 201, 0.21);"
                        >
                            <p
                                class="leading-normal tracking-normal text-13 font-bold text-just-tailwind-black"
                            >
                                {{ time }} min
                            </p>
                        </div>
                    </div>
                    <!-- END -->

                    <!-- SLOT SECTION -->
                    <div
                        v-for="(slot, i) in slots"
                        :key="i"
                        class="pb-6 border-b-2 border-solid border-just-tailwind-gray-300 mt-6"
                    >
                        <!-- DATE SECTION -->
                        <div
                            class="text-left"
                        >
                            <h3
                                class="text-16 leading-normal tracking-normal font-bold text-just-tailwind-black text-left"
                            >
                                {{ slot.date }}
                            </h3>
                        </div>
                        <!-- END -->

                        <!-- TIME SECTION -->
                        <div
                            class="text-left mt-025"
                        >
                            <p
                                class="text-13 leading-normal tracking-normal font-normal text-just-tailwind-black text-left"
                            >
                                {{ slot.time }}
                            </p>
                        </div>
                        <!-- END -->

                        <!-- DURATION SECTION -->
                        <div
                            class="flex items-center justify-between"
                        >
                            <p
                                class="text-13 leading-normal tracking-normal font-normal text-just-tailwind-black text-left"
                            >
                                {{ slot.duration }}
                            </p>
                            <button
                                class="text-just-tailwind-white bg-just-tailwind-primary rounded-md text-13 leading-normal tracking-normal text-center px-2 py-03125"
                            >
                                Choose
                            </button>
                        </div>
                        <!-- END -->
                    </div>
                    <!-- END -->
                    <!-- SEE MORE SLOTS SECTION -->
                    <div
                        class="text-left"
                    >
                        <div
                            class="mt-0625 w-full py-0325 text-center border-2 border-solid border-just-tailwind-black rounded-lg"
                        >
                            <p
                                class="leading-normal tracking-normal text-13 font-bold text-just-tailwind-black"
                            >
                                See more Slots
                            </p>
                        </div>
                    </div>
                    <!-- END -->
                </div>
                <!-- END -->
            </div>
            <!-- END -->
            <!-- MORE THERAPIST SECTION -->
            <div
                class="relative z-50 mt-32"
            >
                <!-- HEADER SECTION -->
                <div>
                    <h3
                        class="text-31 text-left leading-normal tracking-normal font-bold text-just-tailwind-black-900"
                    >
                        More Therapists
                    </h3>
                </div>
                <!-- END -->

                <!-- THERAPIST CARD CONTAINER -->
                <div
                    class="my-16 flex items-baseline overflow-x-scroll"
                >
                    <!-- CARD SECTION -->
                    <div
                        v-for="(data, i) in moreTherapists"
                        :key="i"
                        :class="i == 0 ? 'ml-0' : 'ml-4'"
                    >
                        <!-- IMAGE SECTION -->
                        <div
                            class="w-375 h-auto rounded-08"
                        >
                            <img
                                :src="getImages(data.img)"
                                class="w-full h-full object-contain"
                                alt="Therapists"
                            />
                        </div>
                        <!-- END -->

                        <!-- CONTENT SECTION -->
                        <div
                            class="mt-8"
                        >
                            <!-- NAME SECTION -->
                            <div>
                                <h1
                                    class="leading-normal tracking-normal text-left font-bold text-25 text-just-tailwind-black-900"
                                >
                                    {{ data.name }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- PROFESSION SECTION -->
                            <div
                                class="mt-2"
                            >
                                <p
                                    class="leading-normal tracking-normal text-left font-normal text-16 text-just-tailwind-gray-700"
                                >
                                    {{ data.profession }}
                                </p>
                            </div>
                            <!-- END -->

                            <!-- TAG SECTION -->
                            <div
                                class="mt-4 flex flex-wrap"
                            >
                                <div
                                    v-for="i in data.tags"
                                    :key="i"
                                    :class="i == 'Stress' ? 'ml-0' : 'ml-4'"
                                >
                                    <p
                                        class="leading-normal tracking-normal text-center text-16 font-medium text-just-tailwind-gray-700"
                                    >
                                        {{ i }}
                                    </p>
                                </div>
                            </div>
                            <!-- END -->
                        </div>
                        <!-- END -->

                    </div>
                    <!-- END -->
                </div>
                <!-- END -->

            </div>
            <!-- END -->
        </div>
        <!-- END -->
    </center>
</template>

<script>
export default {
    data () {
        return {
            name: 'Allison May',
            profession: 'Clinical Psychologist',
            amount: 80,
            time: 60,
            quote: "I support women, moms, trauma <br> survivors, and those experiencing <br> invisible illnesses to change patterns and live their best lives",
            moreTherapists: [
                {
                    img: 'alisha3x.png',
                    name: 'Mishay Butler',
                    profession: 'Clinical Psychologist',
                    tags: [
                        'Stress',
                        'Anxiety',
                        'Depression'
                    ]
                },
                {
                    img: 'man3x.png',
                    name: 'Andrew Jonas',
                    profession: 'Clinical Psychologist',
                    tags: [
                        'Stress',
                        'Anxiety',
                        'Depression'
                    ]
                },
                {
                    img: 'alisha3x.png',
                    name: 'Santa Jonas',
                    profession: 'Clinical Psychologist',
                    tags: [
                        'Stress',
                        'Anxiety',
                        'Depression'
                    ]
                },
                {
                    img: 'man3x.png',
                    name: 'Joshu John',
                    profession: 'Clinical Psychologist',
                    tags: [
                        'Stress',
                        'Anxiety',
                        'Depression'
                    ]
                }
            ],
            slots: [
                {
                    date: 'Today, Aug 1',
                    time: '10:00 AM',
                    duration: '30 mins'
                },
                {
                    date: 'Aug 2',
                    time: '10:00 AM',
                    duration: '30 mins'
                },
                {
                    date: 'Aug 3',
                    time: '10:00 AM',
                    duration: '30 mins'
                },
            ],
            tags: [
                {
                    name: "Stress"
                },
                {
                    name: "Anxiety"
                },
                {
                    name: "Depression"
                }
            ],
            reviews: [
                {
                    img: 'women3x.png',
                    name: 'Amber May',
                    desc: "Alison has been nothing but great help in these 2 weeks I've known her. I can already see a difference in my journey. She truly has a listening ear and is eager to understand my situation from my point of view. She never rushes me, she always listens and lets me express myself the best way I think is possible in that moment. I'm feeling hopeful on the great impact that therapy will have on me."
                },
                {
                    img: 'women3x.png',
                    name: 'Josh Ambru',
                    desc: "Alison has been nothing but great help in these 2 weeks I've known her. I can already see a difference in my journey. She truly has a listening ear and is eager to understand my situation from my point of view. She never rushes me, she always ."
                }
            ],
            information: [
                {
                    img: 'mask.svg',
                    desc: 'Licensed Marriage & Family Therapist'
                },
                {
                    img: 'experience.svg',
                    desc: '11 years of Experience'
                },
                {
                    img: 'language.svg',
                    desc: 'Speaks English, Spanish'
                }
            ],
            aboutMe: [
                {
                    title: 'My Background',
                    desc: "I have been in the mental health field for over a decade working in a variety of settings. I've been working with clients continuously for the last 6 years. My work is based in Buddhist psychology, mindfulness practices, somatics (body oriented work), 12 step recovery models, and harm reduction. I teach nonviolent communication to my couples clients especially.",
                },
                {
                    title: 'My Personal Beliefs',
                    desc: "I have been in the mental health field for over a decade working in a variety of settings. I've been working with clients continuously for the last 6 years. My work is based in Buddhist psychology, mindfulness practices, somatics (body oriented work), 12 step recovery models, and harm reduction. I teach nonviolent communication to my couples clients especially.",
                },
            ]
        }
    },
    methods: {
        /**
         * getImages
         * Method to return the
         * required images 
        */
        getImages (img) {
            return require('~/assets/images/' + img)
        }
    }
}
</script>