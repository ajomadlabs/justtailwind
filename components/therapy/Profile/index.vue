<template>
    <center>
        <!-- MAIN SECTION -->
        <div
            style="max-width: 1132px"
        >
            <!-- CONTENT SECTION -->
            <div
                class="lg:flex lg:items-start lg:justify-between"
            >
                <!-- PROFILE SECTION -->
                <div
                    class="xs:w-full lg:w-7/12"
                >
                    <!-- FIRST SECTION -->
                    <div
                        class="lg:flex lg:items-start lg:pb-22625 lg:border-b-2 lg:border-solid lg:border-just-tailwind-gray-300"
                    >
                        <!-- PROFILE IMAGE -->
                        <div
                            class="xs:w-3675 xs:h-3675 lg:w-5150 lg:h-5150"                        
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
                            class="lg:ml-21375"
                        >
                            <!-- NAME SECTION -->
                            <div>
                                <h1
                                    class="xs:mt-8 lg:mt-0 leading-normal tracking-normal xs:text-center lg:text-left font-bold xs:text-31 lg:text-39 text-just-tailwind-black-900"
                                >
                                    {{ name }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- PROFESSION SECTION -->
                            <div
                                class="xs:mt-1 lg:mt-0275"
                            >
                                <p
                                    class="leading-normal tracking-normal xs:text-center lg:text-left font-normal text-16 text-just-tailwind-gray-700"
                                >
                                    {{ profession }}
                                </p>
                            </div>
                            <!-- END -->

                            <!-- AMOUNT SECTION -->
                            <div
                                class="xs:hidden lg:block mt-0525"
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
                                class="xs:mt-8 lg:mt-11875 flex flex-wrap justify-center"
                            >
                                <div
                                    v-for="(tag,i) in tags"
                                    :key="i"
                                    class="px-2 py-2 rounded xs:bg-just-tailwind-blue-100 lg:bg-just-tailwind-tag"
                                    :class="i == 0 ? 'ml-0' : 'xs:ml-045 lg:ml-4'"
                                >
                                    <p
                                        class="leading-normal tracking-normal text-center xs:text-13 lg:text-16 font-bold xs:text-just-tailwind-primary lg:text-just-tailwind-black"
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
                    <!-- QUOTE SECTION -->
                    <div
                        class="xs:block xs:mx-0925 md:mx-20 lg:mx-0 lg:hidden mt-12"
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
                            class="xs:my-0075 lg:my-035 xs:ml-045 md:ml-10 lg:ml-11875"
                        >
                            <p
                                class="text-center leading-normal tracking-normal text-just-tailwind-black xs:text-20 lg:text-31 font-normal"
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
                    <!-- SECOND SECTION -->
                    <div
                        class="xs:mx-4 md:mx-20 lg:mx-0 mt-12 xs:pb-12 lg:pb-22625 border-b-2 border-solid border-just-tailwind-gray-300"
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
                                    class="xs:w-8 xs:h-8 lg:w-12 lg:h-12 rounded-full"
                                >
                                    <img
                                        :src="getImages(info.img)"
                                        class="xs:w-8 xs:h-8 lg:w-auto lg:h-auto py-2"
                                        alt="mask"
                                    />
                                </div>
                                <!-- END -->

                                <!-- TEXT SECTION -->
                                <div
                                    class="text-left ml-4"
                                >
                                    <p
                                        class="text-left leading-normal tracking-normal xs:text-16 lg:text-20 text-just-tailwind-gray-700 font-semibold"
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
                            class="xs:hidden lg:block mt-12"
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
                        class="xs:mx-4 md:mx-20 lg:mx-0 xs:pb-8 lg:pb-22625 border-b-2 border-solid border-just-tailwind-gray-300"
                    >
                        <!-- HEADER SECTION -->
                        <div
                            class="xs:hidden lg:block my-20"
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
                            <div
                                class="xs:mt-8 lg:mt-0"
                            >
                                <h1
                                    class="text-25 text-left xs:text-16 lg:text-25 leading-normal tracking-normal text-just-tailwind-black-900 font-bold"
                                >
                                    {{ data.title }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- DESCRIPTION -->
                            <div
                                class="xs:mt-4 lg:mt-8 lg:mb-16"
                            >
                                <p
                                    class="xs:text-16 lg:text-20 font-normal text-left leading-normal tracking-normal xs:text-just-tailwind-gray-700 lg:text-just-tailwind-black"
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
                    <div
                        class="xs:mx-4 md:mx-20 lg:mx-0 xs:pb-8 lg:pb-0 xs:border-b-2 lg:border-b-0 xs:border-solid xs:border-just-tailwind-gray-300"
                    >
                        <!-- HEADER SECTION -->
                        <div
                            class="xs:my-12 lg:my-20"
                        >
                            <h3
                                class="xs:text-25 lg:text-39 text-left leading-normal tracking-normal font-bold text-just-tailwind-black-900"
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
                                    class="xs:w-8 xs:h-8 lg:w-12 lg:h-12"
                                >
                                    <img
                                        :src="getImages(data.img)"
                                        :alt="data.name"
                                        class="h-full w-full object-contain"
                                    />
                                </div>
                                <h1
                                    class="xs:ml-4 lg:ml-8 xs:text-16 lg:text-25 text-left leading-normal tracking-normal text-just-tailwind-black-900 font-bold"
                                >
                                    {{ data.name }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- DESCRIPTION -->
                            <div
                                class="xs:mt-4 lg:mt-8 xs:mb-8 lg:mb-16"
                            >
                                <p
                                    class="xs:text-16 lg:text-20 font-normal text-left leading-normal tracking-normal text-just-tailwind-black"
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
                    class="xs:hidden lg:block w-843125 border border-solid border-just-tailwind-gray bg-just-tailwind-white rounded-12 py-6 px-104375 shadow-slot"
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
                class="xs:mt-4 xs:mx-4 md:mx-20 xs:mb-32 lg:mb-0 lg:mx-0 lg:mt-32"
            >
                <!-- HEADER SECTION -->
                <div>
                    <h3
                        class="xs:text-25 lg:text-31 text-left leading-normal tracking-normal font-bold text-just-tailwind-black-900"
                    >
                        More Therapists
                    </h3>
                </div>
                <!-- END -->

                <!-- THERAPIST CARD CONTAINER -->
                <div
                    class="xs:my-12 lg:my-16 flex items-baseline overflow-x-scroll"
                >
                    <!-- CARD SECTION -->
                    <div
                        v-for="(data, i) in moreTherapists"
                        :key="i"
                        :class="i == 0 ? 'ml-0' : 'xs:ml-225 lg:ml-4'"
                    >
                        <!-- IMAGE SECTION -->
                        <div
                            class="xs:w-63875 lg:w-375 h-auto rounded-08"
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
                            class="xs:mt-4 lg:mt-8"
                        >
                            <!-- NAME SECTION -->
                            <div>
                                <h1
                                    class="leading-normal tracking-normal text-left font-bold xs:text-20 lg:text-25 text-just-tailwind-black-900"
                                >
                                    {{ data.name }}
                                </h1>
                            </div>
                            <!-- END -->

                            <!-- PROFESSION SECTION -->
                            <div
                                class="xs:mt-1 lg:mt-2"
                            >
                                <p
                                    class="leading-normal tracking-normal text-left font-normal xs:text-13 lg:text-16 text-just-tailwind-gray-700"
                                >
                                    {{ data.profession }}
                                </p>
                            </div>
                            <!-- END -->

                            <!-- TAG SECTION -->
                            <div
                                class="xs:mt-2 lg:mt-4 flex flex-wrap"
                            >
                                <div
                                    v-for="i in data.tags"
                                    :key="i"
                                    :class="i == 'Stress' ? 'ml-0' : 'xs:ml-2 lg:ml-4'"
                                >
                                    <p
                                        class="leading-normal tracking-normal text-center xs:text-13 lg:text-16 font-medium text-just-tailwind-gray-700"
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
            <!-- MOBILE AMOUNT SECTION -->
            <div
                class="xs:block lg:hidden fixed bottom-0 bg-just-tailwind-white w-full py-5 px-4 md:px-20 shadow-slot-mobile"
            >
                <!-- CONTENT SECTION -->
                <div
                    class="flex items-center justify-between"
                >
                    <!-- AMOUNT SECTION -->
                    <div>
                        <p
                            class="leading-normal tracking-normal text-left text-16"
                        >
                            <span class="font-bold text-just-tailwind-black">${{ amount }} / Session</span>
                        </p>
                    </div>
                    <!-- END -->

                    <!-- BUTTON SECTION -->
                    <button
                        class="tracking-normal bg-just-tailwind-primary leading-normal text-just-tailwind-white font-bold text-16 text-center py-3 px-11 rounded"
                    >
                        See Dates
                    </button>
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
            quote: `I support women, moms, trauma <br class="xs:hidden lg:block"> survivors, and those experiencing <br class="xs:hidden lg:block"> invisible illnesses to change patterns and live their best lives`,
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