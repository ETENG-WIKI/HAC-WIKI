## 一 起因
因为项目中有很多配置化的东西，写一条自定义grunt命令，完成不同环境的前台构建。

## 二 修改copy任务
在task路径下，在copy文件中，增加一个任务(参考)：
```
test: {
      src: "<%= config.app %>/buildConfig/config/test",
      dest: "<%= config.app %>/js/constant/config.js"
    }
```
## 三 修改gruntfile.js
拷贝build任务，修改任务名为buildTest，在最上方添加一个子任务copy:test。最后，运行grunt buildTest任务即可。
```
grunt.registerTask('buildTest', [
    'copy:test',
    'clean',
    'prepareHtml',
    'prepareBower',
    'copy:app',
    'copy:framework',
    'useminPrepare',
    'generated',
    'usemin',
    'ngTemplate'
  ]);
```