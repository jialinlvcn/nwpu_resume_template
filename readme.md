# Resume Template (Open Source Version)

一个基于 LaTeX 的简历模板。

## 使用方法

### 第一步：配置个人信息

打开 `resume.tex` 文件，在文件开头的 **"用户自定义配置区"** 中修改以下变量：

```latex
% 个人基本信息
\def\UserName{您的姓名}
\def\UserPhone{您的电话号码}
\def\UserEmail{your.email@example.com}
\def\UserGender{您的性别}
\def\UserAge{您的年龄}
\def\UserDegree{您的学历}
\def\UserAdvisor{导师姓名}
\def\UserHometown{您的籍贯}
\def\UserPoliticalStatus{您的政治面貌}

% 教育经历
\def\UniversityA{大学名称}
\def\MajorMaster{硕士专业名称}
\def\CollegeMaster{学院名称}
\def\MajorBachelor{本科专业名称}
\def\CollegeBachelor{学院名称}

% 研究方向
\def\ResearchDirection{您的研究方向}
```

### 第二步：填写简历内容

根据模板中的提示，逐节填写您的具体信息：

1. **教育经历**：填写您的学校、专业、课程和研究方向
2. **项目经历**：详细描述您参与的项目，包括技术栈、问题、贡献和成果
3. **科研经历**：列出您的研究成果，包括论文题目、期刊/会议、创新点和成果
4. **荣誉奖项**：列出您获得的各种奖项和荣誉
5. **技能专长**：填写您掌握的编程语言、工具和外语能力
6. **自我评价**：简要描述您的个人品质和能力

### 第三步：编译文档

#### 本地编译

0. 确保已经安装 LaTeX 发行版（推荐 TeXLive 或 MiKTeX）
1. 在项目根目录下运行：
   ```bash
   latexmk
   ```
   或直接使用：
   ```bash
   xelatex resume.tex
   ```

#### Overleaf 在线平台

1. 将以下文件上传到 Overleaf：
   - `resume.tex`
   - `resume.cls`
   - `icons/` 文件夹（包含图标）
2. 将编译器设置为 **XeLaTeX**
3. 点击编译按钮

## 宏命令说明

- `\ResumeName{}` 定义简历标题（姓名）
- `\ResumeContact{}` 添加一个联系方式
- `\ResumeContacts{itemA, itemB, itemC}` 添加多个联系方式
- `\ResumeTitle` 渲染标题和联系方式
- `\section{}` 节标题
- `\ResumeItem[]{}[][]`
  - 第1个参数（可选）：PDF 书签内容
  - 第2个参数：项标题，左对齐
  - 第3个参数（可选）：补充信息
  - 第4个参数（可选）：右对齐（如时间）
- `\GrayText{}` 改变文字内容为灰色
- `\ResumeUrl{}{}` 带有下划线的超链接

## 包依赖

## 照片插入

模板支持插入照片，默认已注释。如需使用：

1. 取消 `resume.tex` 中照片相关代码的注释
2. 准备您的照片文件（如 `identification_photo.jpg`）
3. 调整照片大小和位置参数

```latex
\begin{tikzpicture}[remember picture, overlay]
    \node [anchor=north east, inner sep=0.8cm]  at (current page.north east) 
    {\includegraphics[width=2.5cm]{your-photo.jpg}};
\end{tikzpicture}
```

## 注意事项

## 有用的相关资源

- [简历改进指南](https://intdouble.com/resume/)
- [Overleaf 文档](https://www.overleaf.com/learn)
- [LaTeX 入门教程](https://www.latex-project.org/)

## 致谢

本项目主要受到以下项目的启发：
- [hijiangtao/resume](https://github.com/hijiangtao/resume)
- 原始 Resume-NG 项目

本版本已进行脱敏处理，适合作为开源模板分享使用。

## License

本项目采用开源协议，欢迎 Fork 和 Star！