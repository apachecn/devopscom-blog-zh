# 网络研讨会:进化 Jenkins 用户界面

> 原文：<https://devops.com/webinar-evolving-the-jenkins-ui/>

![cloudbees-enterprise-jenkins-logo-(4)](img/cdcc83a8b3b74e8191b1daac4e3a9691.png)Jenkins is the clear #1 continuous integration (CI) and continuous delivery (CD) tool because it is very effective when it comes to automated testing and deployment of software in complex and diverse environments. Jenkins has achieved this position in spite of the fact that it doesn’t look as “trendy” as some of the other tools available in the CI/CD space.In this talk, Gus will detail ongoing efforts to evolve the Jenkins UI. The goal of the initiative is to give Jenkins a more modern look and feel. They’ll talk about the challenges inherent in this effort, as well as some new Jenkins UI building tools and patterns being experimented with at CloudBees.People interested in the Jenkins UI should attend this talk. Please bring your bag of ideas and get involved with this effort.

* * *

## 录音

[https://www.youtube.com/embed/LOmFXFq3Uzg](https://www.youtube.com/embed/LOmFXFq3Uzg)

## 幻灯片

[seoslides embed_id=”69f217917af8″ script_src=”https://devops.com/embed-script/9828/9844/” overview_src=”https://devops.com/slides/9828/” site_src=”https://devops.com” site_title=”DevOps.com” title=” ” /] 

## 问答跟进

| 

*   **How likely are these user interface changes to become core open source software? When can we see them there?**know OSS best. The exact timetable has not yet been determined, but most of it will still be about a year later. It is likely that we will have an experimental war download.

 |

| 

*   **Is there any way to determine which GUI attribute is contributed by which plug-in**I think this is a bit like a feature requirement? JUC West also appeared. It should be something that can appear in the GUI. I agree, it will be very helpful.

 |

| 

*   **What's the difference between ants and Jenkins?**Ants are a bit better quasi-system than Jenkins. In fact, you can add an Ant plugin in Jenkins environment. You usually use Ant to compile java source files. Jenkins coordinates the acquisition of source files from a specific repository, builds these files (usually Jenkins uses Ant through its plug-in), runs and reports some test suites against this build, and then archives or deploys artifacts anywhere. Usually, this requires navigation between multiple computers with their own security restrictions, so Jenkins can also help you manage it.

 |

| 

*   **Which version of Jenkins is this?**This is not only available today, but I am aiming at 1.621-Snapshot Currently, but I will upgrade to the upcoming LTS in December with Jenkins.

 |

| 

*   **I'm interested to see the list of 100 plugins you mentioned (by Daniel? )**Me too. And his community (if you want to join IRC in freenode.net/#jenkins and attend the party and governance meeting, it can be you: http://jenkins.ci.org)

 |

| 

*   **For IRC, I assume that the server is freenode.net?**Yes.

 |

| 

*   **Will there be any dashboard-type build history function in the new GUI**So far, I have been focusing on the creation and configuration of Jenkins UX, because I think it is an entry barrier for new users. Jenkins UX's reading/reporting/analysis I actually think is the part with more long-term value, because you often read more times than you write, so I am eager to join in.  … However, in its core today, it seems to me that Jenkins, a tool, really wants to see the world in the same context of the flat XML file in the folder, because it actually saves its configuration data. To really make a meaningful dashboard, you need to be able to query job configuration and build artifacts according to a wide set of standards, which have nothing to do with the folder where xml files are stored. In addition, in the Jenkins field, some things you care about are computing resources (master/slave/precision). These are also different from the configuration files in folders, and need to be queried as their own first-class entity types.    … So what I want to say is that I think the configuration file is a more direct and urgent solution. Cauliflower for this meal, if you like. I'll want to get it out as soon as possible. The part of the report is actually wine. Now, we give you Bart and Jim in paper cups.    … So there is still a lot of work to be done there.

 |

| 

*   **Have you studied Google Polymer as a UI component of jenkins UI?**I don't have it yet, but I need it now. In fact, I am a Google fan, just as many children like apples. (I also love Apple ... from Seattle, and I even love MS). However, in the near term, we are most concerned about getting JQuery into the core and prototype cleanly. JS has been deprecated. Go first, it's my feeling.

 |

| 

*   **Is there a tutorial about Jenkins' workflow?**Jesse gleeck or KK is a better person to ask this, really. They are also on IRC: so is freenode.net/#jenkins Daniel Becke, who may be a good candidate. My little workflow demonstration is still just fiction.

 |

| 

*   **Will accordion have "Expand All" and "Collapse All" buttons in the new configuration interface? (I will probably inject one if it is not the default)**Yes. In addition, they should be URL controllable so that they can be easily set through links or user contexts. Maybe they should remember what you finally opened? ... what needs mending must be correct.

 |

| 

*   **What impact does  UI change have on the background job configuration? Is the configuration still stored in XML format?**none. The post string remains the same. Since then, Jenkins has been Jenkins.

 |

| 

*   **Can the Create Project screen be configured?**At the moment, no, but ideally it is. At present, how to create, manage and update these categories is still a big problem. When searching for plugins, the same category should appear to help associate what plugins generate what UI. I hope to get guidance from the community.

 |

| 

*   **How does the workflow adapt to the new user interface?**In some aspects, the new configuration page is about enhancing the more traditional freelance work instead of workflow. However, the last point of my demonstration about script builder is about workflow. Plugin Manager is about plugins, so it applies to both.

 |

| 

*   **In this workflow, how do I inform the labor to wait for approval?**Therefore, workflow approval can be completed through the web GUI. But to get a real notification, you need to program it into your workflow. So you can use Jenkins to trigger emails, or text messages, or HipChat, or Slack, or almost anything. As these plug-ins are increasingly customized for workflows, you will get very good workflow syntax for instantiating these actions. When my script generator is adopted, you will have a friendly button, you can drag it onto the stage, and it will inform you before the manual checkpoint.

 |

| 

*   **Is the custom plug-in still supported?**Yes. Although there is support, there is also support. The highest level of support for a plug-in is a customized workflow DSL, which can simplify the syntax of interacting with the plug-in through Groovy in the workflow. But existing plug-ins don't need to use this level of support in Jenkins files/Groovy scripts. On the contrary, the syntax of accessing plug-ins may be more complicated.  … Some plug-ins are freestyle-specific. In this case, they no longer make sense in the workflow.  … Daniel Becke or Jesse Gehrig may be more suitable to answer this question, however …

 |

| 

*   **When Docker is built, will the performance of sonar scanning be improved? According to my experience, it takes sonar more than 20 minutes to use jenkins plug-in, while it takes 3 minutes to use maven plug-in**. Does this require GUI rendering or actual building and running? I'm not sure if I fully understand this question, but anyway, I can't answer many questions about Jenkins' performance. I know a considerable performance problem, especially in the configuration form. I believe this problem will be solved in the new GUI, but this is not the build performance, it is only the form rendering performance.

 |

| 

*   **I like the graphical configuration. Thanks. Scripts for complex workflows look a bit daunting.**Cool. Yes, my main and first goal is to enable people to quickly sketch and deploy an actual workflow that reasonably reflects about 80% of use cases. No GUI can be as flexible as scripts, but I don't think most people need 95% of the time to get started and see the benefits of versionable and robust profile formats.

 |

| 

*   **Will efforts be made to make the mobile user interface friendly to mobile administrators?**Absolutely. Especially in the TBD reading/reporting end of the user interface, but anything new needs to meet the quite high equipment response requirements. Today, Jenkins GUI just doesn't respond. This is terrible.

 |

| 作为一个插件开发者，我需要把实现 ui 的源代码从 jelly 或 groovy 改成其他语言/技术吗？或者它是兼容的吗？因此，您不需要改变您正在做的任何事情，除非您已经构建了一个插件 GUI，它具有直接依赖于 behavior.js、hudson-behavior.js 或现有 DOM 结构的特定内容的自定义脚本(您在客户端中做了一些事情，要求您的或其他一些输入位于特定的<表><tr><TD>DOM 遍历路径中)。  ……我相信两件事会以越来越快的速度继续发生。新插件作者不打算用 Jelly 和 Prototype.js 编写 GUI，而是使用一些更现代的客户端 MVC 方法，如 Angular，其中 GUI 与 REST api 交互，而不是直接从服务器呈现的 dom。这是一种与 Jelly 不同的工作模式，可能不太直接，但是找到关于如何使用 JQuery、Agile、Handlebars 等工具的文档要比在 Jelly 上找到文档容易得多。Jelly 中手势和控件的响应能力和广度已经远远落后于现在 web UI 开发的主流。所以我认为插件开发者，如果他们还没有的话，会想要更好的工具。  我也认为人们会被工作流或类似的东西所吸引。因为工作流的 UI 首先是一个脚本，所以为一个插件制作一个 GUI 可能是一件完全不同的事情。…这取决于插件试图做什么…所以，新插件甚至升级现有插件以配合工作流很可能需要新的技术集，不仅仅是因为现有的 Jenkins GUI 正在发生变化，还因为新插件希望做不同的和更好的事情。 |

| 

*   **Are there any other connectors for source control tools like CVS and Dimensions?**I'm not sure which connector plug-ins already support workflow, or how deep this support is. Because Jenkins has plug-ins that provide access to these SCMs, you can use workflow to get those source trees. The higher level of workflow support of these plug-ins will mean more elegant interactive workflow syntax. At present, my GUI script generator is still fictitious. My plan is to add GUI buttons for the most popular SCMs, and I will try to cover up the syntax, no matter how clumsy it is.  … According to the way I built the initial prototype, there is already a fairly clear extension point where buttons can be added. When buttons are dragged into a stage, some Groovy syntax will be generated. Therefore, I will add the initial settings according to the community feedback, and then the community can continue to add their own settings.

 |

| 

*   **What compatibility issues do existing plug-in developers need to pay attention to?**For plug-ins that interact with free jobs, or in fact, most job types that are not workflows, plug-in developers should expect the page DOM structure to change. For whatever reason, if they find themselves entering some custom scripts to traverse the DOM to compare one setting with another, it will break.  In addition, hudson-behaviors.js itself also has many DOM traversal functions, such as "findFollowingTR". In some cases, the signatures of these functions may need to be changed, and the DOM structure returned by them may also change. If a plug-in uses something that should be an internal function, they are likely to crash.  Finally, the page geometry will change. This may seem so superficial and obvious, who cares, but sometimes changing the column width can cause important parts of the GUI to be hidden or inaccessible. This is a breakthrough as important as other breakthroughs.    … So in order to solve these possible vulnerabilities, we will look for 20 to 100 plug-ins for testing. We haven't made a list yet, let alone conducted any tests, so this is really the key next step.    I don't see too many braking problems with the change of plug-in manager, although I want to add additional sorting and display functions to the GUI, which means that if plug-ins want to take advantage of new functions in the GUI, the GUI will need more metadata than the existing ones. This won't break things, but plugin authors may want to go back to their plugins and fill in any new metadata. Most likely, richer descriptions, better category selection, and possibly icons.

1.  **I haven't met many Jenkins, but I didn't really get what I had, which was embarrassing for all the reasons mentioned by Gus. This looks great. When can we have it? Tom and I, and now our newcomer Keith (actually not a newcomer at all, just healthier than me), are busy typing as fast as possible and lobbying the community to say that our vision is more or less correct. We have a very interesting initial plugin selection GUI that may make this year's final LTS (I didn't demonstrate it), which is still a good improvement. There will be a lot of JS libraries bundled in it, which will realize most of what I have shown in this demonstration. Our hope is that with each LTS, we will be able to launch an additional GUI puzzle. It may start with creating and configuring GUI, which will be LTS in the middle of the year. I hope Jenkins will be like this in a year.  … At the same time, we are trying to figure out how to best launch the preview version so that people can play it and send me hate mail. T54**

 |

| 

*   **Is there any way to test the Jenkins plugin on the front end? Will that also improve?**A major and almost blocked part of this work used to be the customized and somewhat broken version of HTMLUnit in the core, which greatly hindered the inclusion of libraries other than prototypes in Jenkins and the use of these libraries to write code in some testable way. Our new method of rebuilding Jelly control is the foundation of Jenkins configuration page, which is usually shared by all plug-ins that need to send data back to Jenkins. There is already a test strategy to support our design. These Jelly form controls are extensible in today's Jenkins and will always be maintained. Our hope is that any plug-in that adds custom controls will follow the same design and test pattern that we built in the core.  … So this is a long answer, but the short answer is yes! Today, building GUI widget in your Jenkins plugin is a bit mysterious. Most people copy what they see others do and crack it. The only test is, well … it works for me. This is not good, and it is a basic part of what we hope to change.  … or a long answer …  Node.js and Jasmine are the specific tools we use.

1.  **When is the expected launch date of this workflow feature?**Workflow feature is the latest concept I demonstrated, but it may also be the easiest to implement in many aspects. As a script generator, it can be hosted anywhere, and then you just need to paste your generated workflow script into any existing Jenkins GUI. Better yet, submit it to your source code.    …。 However, at present, it actually has no formal road map.  Assuming that the reaction to it is still positive, I would think that the change will be quite rapid. T51

 |

* * *

## 你的主持人![alan_new_head_shot](img/16e973f8e9fd656a095a85e6415bb5b0.png)

**Alan Shimel，总编辑 DevOps.com**，Alan 是安全和技术界经常被提及的人物，也是行业和政府活动中广受欢迎的演讲者，他将强大的商业背景与深厚的技术知识相结合，帮助建立了几家成功的技术公司。

## 关于小组成员

**![Reiber](img/eebda8df2d8f2e8559dce1217f3340eb.png) Gus Reiber，CloudBees 公司高级用户界面开发人员**

身高 5 英尺 8 英寸，体重 190 磅(41-43-40)的蓝眼睛摩羯座的格斯是一个实用性很强的人。凭借 20 年的设计和 UI/UX 经验，Gus 与大大小小的公司打过交道，包括大量的初创公司和首次发布的软件产品。其中最著名的是 Allaire、Macromedia、Adobe 和日立数据系统公司。现在在 CloudBees，Gus 正在寻求与 CloudBees 社区交朋友，并将 Jenkins 带入下一代用户体验美好时代。女士们，排成一队…