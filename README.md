# copilot-chinese中文文档（非官方）
# Getting Started with GitHub Copilot in JetBrains 

```
- [Installing the JetBrains extension](#installing)
- [Seeing your first suggestion](#first-suggestion)
- [Choosing alternate suggestions](#alternates)
- [Getting more suggestions](#more-suggestions)
- [Generating code from a comment](#code-from-comment)
- [More examples](#more-examples)
- [Keyboard shortcuts](#shortcuts)
- [Enabling or disabling GitHub Copilot](#enabling)
- [Learn More](#more)
```
- [安装JetBrains扩展](#installing)
- [来看看给你的第一个建议](#first-suggestion)
- [在可供选择的选项中进行选择](#alternates)
- [获取更多的建议](#more-suggestions)
- [从注释生成代码](#code-from-comment)
- [更多案例](#more-examples)
- [快捷键](#shortcuts)
- [打开或关闭](#enabling)
- [更多](#more)

<a name="installing"></a>
## 1. Installing the JetBrains extension
## 1. 安装JetBrains扩展

1. We have tested with the following JetBrains IDEs: IntelliJ and PyCharm versions 2021.2 and above.
  经过测试，IntelliJ与PyCharm请使用2021.2及以上版本。

2. From the JetBrains marketplace, search for 'github copilot'.  (You must include the 'github' to avoid other plug-ins with similar names.)
  通过JetBrains的marketplace，搜索‘github copilot’。（请务必包含‘github’以避免检索到其他扩展）
   <img src='resources\search-for-github-copilot_jetbrains.png' width="600px" alt="Search for `github copilot`"/>

3. Click the 'Install' button.
  点击‘安装’按钮.

4. Accept the Third-Party Plugins Privacy Notice.
  接受第三方扩展的隐私通知。
5. Exit and restart the IDE.
  退出并重启IDE
6. In the Tools menu you will now see a GitHub Copilot option.
  现在，你可以在‘工具’选项卡中看见 Github Copilot 选项
  <img src='resources\sign-in_jetbrains.png' width="600px" alt="Tools GitHub Copilot option`"/>
  
7. Login to GitHub Copilot using the device auth flow and authorized GitHub Copilot IntelliJ plugin with your GitHub Account in an external browser.
   通过设备授权码登录GitHub账号
8. Read and agree to the GitHub Copilot additional telemetry terms.
  阅读并同意GitHub copilot文档（翻译为：遥测术语）
9. Click `OK`.
 点击‘OK’
   Now when you start editing, you should see GitHub Copilot suggestions.
  现在，当你进行编程时，你就能看见coplilot提供的建议
   If you receive the following message, you have not yet been added to the GitHub Copilot Technical Preview.
  如果你看到的是如下的信息，表明你还未被添加到预览队列（即无内测资格）
   <img alt="Not in the preview" src="resources/not-in-preview_jetbrains.png" width="600"></img>

   The Technical Preview is open to a limited number of testers. To join the 
   waitlist, visit [copilot.github.com](https://copilot.github.com).

   Having problems installing? Visit the [Feedback forum](https://github.com/github/feedback/discussions/categories/copilot-feedback).

<a name="first-suggestion"></a>
## 2. Seeing your first suggestion
## 2.来看看给你的第一个建议
GitHub Copilot provides code suggestions for dozens of languages and a wide variety of frameworks, 
but it works especially well for Python, JavaScript, TypeScript, Ruby, Java, and Go. 
The following samples are in Java, but other languages will work similarly.
GitHub Copilot提供几十种语言和各类框架的编写建议，但是其对Python, JavaScript, TypeScript, Ruby, Java, Go的支持非常好，下面以java为例进行演示，其他语言同理。

1. Create a new Java (.java) file.
创建一个新的java(.Java)文件
2. Create a class by typing
创建一个类之后输入
```class Test ```

   Copilot will suggest a class body.
  copilot将会对class主体提供建议
   <img alt="Class code suggested by GitHub Copilot" src="resources\suggestion-class_jetbrains.png" width="600"></img>
   
   Press `tab` to accept the suggestion.
  按下`tab`键接受建议
3. Below the bracket of the `main` function, type the following function header:
  在"main"函数的括号下方，输入如下功能函数的函数头
   ```
   int calculateDaysBetweenDates(
   ```

3. GitHub Copilot will automatically suggest an entire function body in grayed text, as shown below. 
The exact suggestion may vary.
  它将会自动的建议并填充功能主题，像展示的这样，可能会提供多个建议
   <img alt="Code suggested by GitHub Copilot" src="resources\suggestion-function-body_jetbrains.png" width="600"></img>

4. Press `Tab` to accept the suggestion.
  按下`tab`键接受建议
GitHub Copilot will attempt to match your code's context and style. You can edit the suggested code as you choose.
它会尝试与你的编写风格和内容进行适配，你可以按照自己的想法对建议进行修改
<a name="alternates"></a>
## 3. Choosing alternate suggestions
## 3.在可供选择的选项中进行选择
For any given input, GitHub Copilot can provide multiple suggestions. 
As the developer you are always in charge; you can select which suggestion to use, or reject them all.
对于任何给定的输入，它可以提供多种建议，作为开发者的你可以掌握一切，你可以选择其中一个，也可以拒绝所有。
1. Remove the function you entered and type the following again:
删除并输入如下内容
   ```
   int calculateDaysBetweenDates(
   ```

2. GitHub Copilot will again show you a suggested completion.
它会提供建议
3. Instead of pressing `Tab`:
代替`tab`键的操作如下：
   * On macOS, press `Option`+`]` for next or `Option`+`[` for previous.
   * 在macOS中，按下`Option`+`]`查看下一个或者`Option`+`[`查看前一个
   * On Windows or Linux, press `Alt`+`]` for next or `Alt`+`[` for previous.
   * 在Windows或者Linux中，按下`Alt`+`]`查看下一个或者`Alt`+`[`查看前一个
  
   GitHub Copilot will cycle through other alternative suggestions.
它会循环的提供可供你选择的建议
4. When you see a suggestion you like, press `Tab` to accept it.
当你看到你想要的建议时，按下`tab`键来选择它

5. If you don't like any of the suggestions, press `Esc`.
如果你都不喜欢，按下`esc`来取消
<a name="more-suggestions"></a>
## 4. Getting more suggestions
## 4.获取更多的建议
Sometimes, you may not want to use any of the initial suggestions. 
You can ask GitHub Copilot to return more.
有时，您可能不想使用任何初始建议。
您可以要求GitHub Copilot返回更多。
1. Remove the function you entered and type the following again:
删除并输入如下内容
   ```
   int calculateDaysBetweenDates(
   ```

2. GitHub Copilot will again show you a suggested completion.
GitHub Copilot 将再次向您显示建议的完成情况。
3. Open GitHub Copilot.
打开GitHub copilot
   * On macOS, press `Option`+`Enter`.
   * 在macOS中，使用`Option`+`Enter`
   * On Windows or Linux, press `Alt`+`Enter`.
   * 在Windows或者Linux中，使用`Alt`+`Enter`

   <img alt="Open GitHub Copilot" src="resources\command-palette_jetbrains.png" width="600"></img>

   Select "Open Copilot". GitHub Copilot will open a new tab and suggest multiple options, as shown below.
  选择打开copilot，GitHub Copilot将打开一个新选项卡并提供多个选项，如下所示。
   <img alt="Suggestions window" src="resources\completions-pane_jetbrains.png" width="600"></img>

4. Pick a suggestion that you want to use, then click "Accept solution."
选择要使用的建议，然后点按"接受"。
5. If you don't like any of the returned suggestions, just close the suggestions tab.
如果您不喜欢任何返回的建议，只需关闭建议选项卡即可。
<a name="code-from-comment"></a>
## 5. Generating code from a comment
## 5.从注释生成代码
GitHub Copilot can understand significantly more context than most code assistants, 
and can generate entire functions from something as simple as a comment. 
GitHub Copilot可以比大多数代码助手理解更多的上下文，
并且可以从像注释这样简单的东西生成整个函数。
1. Remove the function you entered and type the following:
删除并输入如下内容
   ```
   // find all images without alternate text
   // and give them a red border
   void process() {
   ```

2. GitHub Copilot will automatically suggest an implementation:
GitHub Copilot 将自动实现一个建议
   <img alt="Suggestions window" src="resources\code-from-comment_jetbrains.png" width="600"></img>

<a name="more-examples"></a>
## 6. More examples
## 6.更多例子
GitHub Copilot has even more capabilities. 
GitHub Copilot有非常多的功能
Check out the examples on [copilot.github.com](https://copilot.github.com) to see more, 
点击连接查看更多[copilot.github.com](https://copilot.github.com)


this repository for the latest examples from us and the community.
这个仓库将用于我们最新的示例和交流
Got an example of your own? We welcome you to share it on our [Feedback forum](https://github.com/github/feedback/discussions/categories/copilot-feedback).
分享你自己的示例？我们欢迎你分享到我们的论坛[Feedback forum](https://github.com/github/feedback/discussions/categories/copilot-feedback)
<a name="shortcuts"></a>
## 7. Keyboard shortcuts
## 7.快捷键
The following lists the most common keyboard shortcuts relevant for GitHub
Copilot. If you wish to rebind them, check out [the configuration guide](configuring.md).

* Accept an inline suggestion: `Tab`.
接受——`tab
* Dismiss an inline suggestion: `Esc`.
忽视——`Esc`
* Show next inline suggestion: `Alt + ]` or `Option + ]`.
下一个建议——`Alt + ]` `Option + ]`
* Show previous inline suggestion: `Alt + [` or `Option + [`.
上一个建议——`Alt + [` `Option + [`
* Trigger inline suggestion: `Alt + \` or `Option + \`.
ps：这个不好翻译，请自行尝试
* Open Copilot (up to 10 suggestions in separate pane): `Alt + Enter` or `Option + Enter` then pick "Open Copilot".
打开copilot——`Alt + Enter` `Option + Enter` "Open Copilot"
<a name="enabling"></a>
## 8. Enabling and disabling GitHub Copilot
## 8.打开或关闭
There's a setting to turn on or off the automatic completions. You can find the setting at `Preferences... > Languages & Frameworks > GitHub Copilot`.
设置路径`Preferences... > Languages & Frameworks > GitHub Copilot`
   <img alt="The GitHub Copilot preferences" src="resources\preferences.png" width="600"></img>

You can also logout (or login) from Copilot from the `Tools`/`GitHub Copilot` menu.
你也可以登录或登出，路径`Tools`/`GitHub Copilot`
   <img alt="The GitHub Copilot submenu in the Tools menu" src="resources\logout_jetbrains.png" width="600"></img>

<a name="more"></a>
## 9. Learn More
## 9.更多
To learn more about configuring GitHub Copilot, go to the [documentation table of
contents](README.md).
查看更多，前往[documentation table of
contents](https://github.com/github/copilot-docs/blob/main/README.md)
