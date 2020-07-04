<template>
   <div>
       <vue-ueditor-wrap   :config="config"   ref="ueditor"   @ready="ready"   style="height:700px;"></vue-ueditor-wrap>
   </div>    
</template>
<script>
import VueUeditorWrap from 'vue-ueditor-wrap'
export default {
  components: {
    VueUeditorWrap
  },
  data() {
    return {
      config: {
        UEDITOR_HOME_URL: "/UEditor/",

        autoHeightEnabled: false,

        initialFrameHeight: 500,

        initialFrameWidth: "100%",

        toolbars: [
          [
            "fullscreen",
            "source",
            "|",
            "undo",
            "redo",
            "|",

            "bold",
            "italic",
            "underline",
            "fontborder",
            "strikethrough",
            "superscript",
            "subscript",
            "removeformat",
            "formatmatch",
            "autotypeset",
            "blockquote",
            "pasteplain",
            "|",
            "forecolor",
            "backcolor",
            "insertorderedlist",
            "insertunorderedlist",
            "selectall",
            "cleardoc",
            "|",

            "rowspacingtop",
            "rowspacingbottom",
            "lineheight",
            "|",

            "customstyle",
            "paragraph",
            "fontfamily",
            "fontsize",
            "|",

            "directionalityltr",
            "directionalityrtl",
            "indent",
            "|",

            "justifyleft",
            "justifycenter",
            "justifyright",
            "justifyjustify",
            "|",
            "touppercase",
            "tolowercase",
            "|",

            "link",
            "unlink",
            "anchor",
            "|",
            "imagenone",
            "imageleft",
            "imageright",
            "imagecenter",
            "|",

            "simpleupload",
            "insertimage",
            "|",

            "horizontal",
            "date",
            "time",
            "spechars",
            "snapscreen",
            "|",

            "inserttable",
            "deletetable",
            "insertparagraphbeforetable",
            "insertrow",
            "deleterow",
            "insertcol",
            "deletecol",
            "mergecells",
            "mergeright",
            "mergedown",
            "splittocells",
            "splittorows",
            "splittocols",
            "charts"
          ]
        ],

        // 显示字数

        wordCount: true,

        // 上传图片路径

        // serverUrl: 'http://35.201.165.105:8000/controller.php'

        serverUrl: "/img/upload",

        pasteplain: true, //是否默认为纯文本粘贴。false为不使用纯文本粘贴，true为使用纯文本粘贴

        autotypeset: {
          mergeEmptyline: true, //合并空行

          removeClass: true, //去掉冗余的class

          removeEmptyline: true, //去掉空行

          imageBlockLine: "center", //图片的浮动方式，独占一行剧中,左右浮动，默认: center,left,right,none 去掉这个属性表示不执行排版

          pasteFilter: false, //根据规则过滤没事粘贴进来的内容

          clearFontSize: false, //去掉所有的内嵌字号，使用编辑器默认的字号

          clearFontFamily: false, //去掉所有的内嵌字体，使用编辑器默认的字体

          removeEmptyNode: false, // 去掉空节点

          //可以去掉的标签

          removeTagNames: { br: 1 },

          indent: false, // 行首缩进

          indentValue: "" //行首缩进的大小
        }
      }
    };
  }
};
</script>
