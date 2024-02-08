# com-icon
公共字体图标库

> [字体图标库地址](https://www.iconfont.cn/manage/index?spm=a313x.user_detail.i3.22.5dc63a81mvyWQj&manage_type=myprojects&projectId=3728577)

## 更新说明
1. 更新字体图标库

2. 下载字体图标库, 复制文件夹下所有文件到**dist**目录下

3. 更新**package.json**文件**version**版本

4. 提交项目**github**仓库

5. 发布到[**npm**](https://www.npmjs.com/package/com-icon)


## 使用说明
1. 方式一(推荐):
    
    使用**antd**自定义图标

    ```jsx
    // custom-icon组件
    import { createFromIconfontCN } from '@ant-design/icons'
    import comIcon from 'com-icon'

    const CustomIcon = createFromIconfontCN({
        scriptUrl: [comIcon],
    })

    export default CustomIcon
    ```
   ```jsx
    // 使用custom-icon组件
    <CustomIcon type="icon-xxx"/>
    ```

2. 方式二:
   - 第一步: 引入项目下面的**fontclass**代码:
       ```html
     <link rel="stylesheet" href="./iconfont/css">
       ```
   - 第二步: 挑选相应图标并获取类名, 应用于页面:
       ```html
       <span class="comIcon icon-xxx" />
       ```

## git commit rules

```格式: <type>(scope): <subject>```

- type: 修改类型
    - feat: 新特性
    - fix: 修改问题
    - refactor: 代码重构
    - docs: 文档修改
    - style: 代码格式修改, **不是css修改**
    - chore: 其他修改, 例如构建流程、依赖管理.
    - revert: 用于撤销以前的commit
- scope: 影响范围. 一般为自己代码的模块名.
- subject: 概述. 建议符合 [50/72](https://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) 格式
