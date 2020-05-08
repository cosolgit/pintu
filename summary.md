### 总结:
- 图片每一个原始位置用 correctX 和 correctY 记录了,
- 最后一个透明,位置不变,其他的打乱顺序,
- 点击与透明相邻的,交换 left 和 top 实现切换位置
- (验证相邻透明与点击的 left 相等高度相差一个 height || top 相等宽度相差一个 width 即为相邻)
- 每次点击校验每一个的 currentX 和 currentY 是否与 left,top 相同,相同即拼好了

