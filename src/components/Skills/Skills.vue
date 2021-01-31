<template>
  <div class="w-full text-left p-3 mt-5">
    <h1>Skill</h1>
    <h2 class="mt-4">プログラミング言語</h2>
        <div class="bg-white shadow-md rounded my-2">
            <table class="text-left w-full border-collapse"> <!--Border collapse doesn't work on this site yet but it's available in newer tailwind versions -->
            <tbody>
                <tr>
                <td class="py-4 px-6 w-40 border-b border-grey-light">さわっただけ</td>
                <td class="py-4 px-6 border-b border-grey-light">
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Python</p>
                </td>
                </tr>
                <tr>
                <td class="py-4 px-6 w-40 border-b border-grey-light">個人開発で使用</td>
                <td class="py-4 px-6 border-b border-grey-light">
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">PHP</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Dart</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Ruby</p>
                </td>
                </tr>
                <tr>
                <td class="py-4 px-6 w-40 border-b border-grey-light">研究活動で使用</td>
                <td class="py-4 px-6 border-b border-grey-light">
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">C++</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">VHDL</p>
                </td>
                </tr>
                <tr>
                <td class="py-4 px-6 w-40 border-b border-grey-light">講義で学んだ</td>
                <td class="py-4 px-6 border-b border-grey-light">
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Java</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">C</p>
                </td>
                </tr>
            </tbody>
            </table>
        </div>

    <h2 class="mt-4">ソフトウェア/インフラ</h2>
        <div class="bg-white shadow-md rounded my-2">
            <table class="text-left w-full border-collapse"> <!--Border collapse doesn't work on this site yet but it's available in newer tailwind versions -->
            <tbody>
                <tr>
                <td class="py-4 px-6 w-40 border-b border-grey-light">個人開発で使用</td>
                <td class="py-4 px-6 border-b border-grey-light">
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Fusion360</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Firebase</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Cloud9</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">AWS S3</p>
                </td>
                </tr>
                <tr>
                <td class="py-4 px-6 w-40 border-b border-grey-light">趣味で使用</td>
                <td class="py-4 px-6 border-b border-grey-light">
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Blender</p>
                    <p class="inline-flex items-center px-3 py-1 bg-gray-200 text-gray-700 rounded-full m-1">Unity</p>
                </td>
                </tr>
            </tbody>
            </table>
        </div>

</div>
</template>


<script>

export default {
    name: "skill",
}
</script>