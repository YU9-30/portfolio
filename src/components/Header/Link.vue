<template>
    <div class="flex flex-wrap">
        <a class="" v-for="link in links" :key='link.url' :href= link.url >
            <button class="m-1 font-medium py-1 px-2 bg-white rounded text-gray-700 bg-gray-100 border border-gray-300 hover:bg-blue-600 hover:text-white">
            {{ link.display_name }}
            </button>
        </a>
    </div>
</template>

<script>
export default {
  name: "links",
  data() {
    return {
        links : [
            {
                url: 'https://twitter.com/yukyu30',
                display_name: 'Twitter',
            },
            {
                url: 'https://github.com/yukyu30',
                display_name: 'Github',
            },
            {
                url: 'https://zenn.dev/yu_9',
                display_name: 'Zenn',
            },
            {
                url: 'https://note.com/yukyu30',
                display_name: 'note',
            },
            {
                url: 'https://blog.yukyu.net',
                display_name: 'blog',
            },
        ]
    };
  },
};
</script>