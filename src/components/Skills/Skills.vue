<template>
  <div class="w-full text-left p-3 mt-5">
    <h1>Skill</h1>
    <h2 class="mt-1">プログラミング言語</h2>
    <table class="table-auto">
                    <tbody>
                        <tr>
                            <td>さわっただけ</td>
                            <td>Python</td>
                        </tr>
                        <tr>
                            <td>個人開発で使用</td>
                            <td>PHP(Laravel), Dart(Flutter),Ruby(Ruby on Rails)</td>
                        </tr>
                        <tr>
                            <td>研究活動で使用</td>
                            <td>C++, VHDL</td>
                        </tr>
                        <tr>
                            <td>講義で学んだ</td>
                            <td>Java, C</td>
                        </tr>
                    </tbody>
        </table>
    <h2 class="mt-1">ソフトウェア/インフラ</h2>
      
  </div>
</template>


<script>

export default {
    props: ['work'],
    name: "work-modal",
    data() {
        return {
            showModal: false,

        }
    },
    methods: {
        closeModal:function(){
            this.$emit('close');
        }
    },
}
</script>