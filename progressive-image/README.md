# 渐进式图片

渐进式加载是一种优化交互体验的方案。

普通图片的加载是随着图片的下载数据的完成度，逐渐从上至下加载的。

如果浏览器只收到了图片文件数据的一半，那么就只会显示图片的上半部分。

而渐进式图片的加载则是先显示图片整体的一个模糊效果，随着下载的完成度，逐步加载清晰的图片。

目前常用的实现方案有两种：1. 使用 progressive 格式的图片；2.占位图 + CSS 模糊效果。

## progressive image

在生成图片时通常都是 baseline 标准型图片。使用 PS 生成 jpeg 格式的图片时，可以选择 progressive 连续型格式。

两种格式有相同的尺寸和图像数据，扩展名也相同，唯一区别就是两者显示方式不同。

## 占位图 + CSS 模糊效果

目前业界主流的方案是使用占位图 + CSS 模糊效果。像百度的图片搜索结果，就是使用这种方案。

具体实现方式查看 index.html

## 开源推荐

[blurhash](https://github.com/woltapp/blurhash)是图像占位符的压缩表示。

## 参考

- [MDN-图片占位符](https://developer.mozilla.org/zh-CN/docs/Web/Progressive_web_apps/Tutorials/js13kGames/Loading#%E5%9B%BE%E7%89%87)
- [大伟聊前端-渐进式图片](https://www.bilibili.com/video/BV1Q24y1L7ew/?spm_id_from=333.337.search-card.all.click&vd_source=dce7b1ab94acfc972ab20009a0109fd3)
- [渡一-渐进式图片](https://www.bilibili.com/video/BV1GssYeAEAB/?spm_id_from=333.337.search-card.all.click&vd_source=dce7b1ab94acfc972ab20009a0109fd3)
