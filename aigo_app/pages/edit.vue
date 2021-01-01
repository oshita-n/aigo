<template>
    <div>
        <div class="mavonEditor">
            <no-ssr>
            <mavon-editor :toolbars="markdownOption" :language="'ja'" v-model="handbook"/>
            </no-ssr>
        </div>
        <br>
        <div>
        <v-row
            align="center"
            justify="space-around"
        >
            <v-btn
            rounded
            color="success"
            to="/" nuxt
            >
            <v-icon left>
                mdi-home
            </v-icon>
            トップページに戻る
            </v-btn>
        </v-row>
        </div>
    </div>
</template>
<script>
export default {
  data() {
    return {
      markdownOption: {
        bold: true,
        italic: true,
        header: true,
        underline: true,
        strikethrough: true,
        mark: true,
        superscript: true,
        subscript: true,
        quote: true,
        ol: true,
        ul: true,
        link: true,
        imagelink: true,
        code: true,
        table: true,
        fullscreen: true,
        readmodel: true,
        htmlcode: true,
        help: true,     
      },
      handbook: "#### Markdown"
    };
  }
};
</script>
 
<style scoped>
.mavonEditor {
  width: 100%;
  height: 100%;
}
</style>