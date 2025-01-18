# The top 5 open-source RPA frameworks—and how to choose

**Matthew David**  
Digital Leader, Accenture

_Original article at https://techbeacon.com/enterprise-it/top-5-open-source-rpa-frameworks-how-choose_

_Published 15 December 2020_


In many organizations, the first step toward automation and artificial intelligence/machine learning is the adoption of robotic process automation (RPA) technology.

Many enterprises are using RPA to improve efficiencies in costs and in IT processes. In many cases, reducing errors, time, costs, and redundant actions can improve the workflow for customers and other stakeholders.

At its core, RPA helps organizations automate defined, multi-step, manual tasks that are done in high volume. RPA does this by creating software robots that copy human actions to interact with existing application interfaces.

RPA has the potential to reduce costs by 30% to 50%. It is a smart investment that can significantly improve the organization's bottom line. It is very flexible and can handle a wide range of tasks, including process replication and web scraping.

RPA can help predict errors and reduce or eliminate entire processes. It also helps you stay ahead of the competition by using intelligent automation. And it can improve the digital customer experience by creating personalized services.

One way to get started with RPA is to use open-source tools, which have no up-front licensing fees. Below are five options to consider for your first RPA initiative, with pros and cons of each one, along with advice on how to choose the right tool for your company.

## Why open source?

At Accenture, my team mostly implements RPA using commercial tools, but we also work with open-source tools and may use a combination for a given client. That said, open-source options are an easy way to dip your toe into the RPA waters without making a major investment in software.

When compared to commercial RPA tools, open source reduces your cost for software licensing. On the other hand, it may require additional implementation expense and preparation time, and you'll need to rely on the open-source community for support and updates. (For more detail on some potential drawbacks, see the discussion in "With AIOps, think twice before going open source.")

Yes, there are trade-offs between commercial and open-source RPA tools—I'll get to those in a minute. But when used as an operational component of your RPA implementations, open-source tools can improve the overall ROI of your enterprise projects. Here's our list of contenders.

### 1. Taskt

Formerly called sharpRPA, Taskt is a free C# program, built using the .NET Framework, that features an easy-to-use drag-and-drop interface that lets you automate processes without any coding.

My teams often work with customers that have only C# development skills, and Taskt is a good tool for C#-centric teams to use to get started with RPA.

You can explore Taskt by going through the examples on GitHub, where you'll also find a step-by-step guide to setting up your task automation process. Many of our developers have a strong Microsoft/Azure background and discover that it is much easier to create scripts with Taskt using C#. There is a Microsoft influence in the tool that will benefit teams that prefer Visual Studio or Azure development environments.

**Bottom line:** Taskt is an excellent tool to use if your team is used to developing Microsoft C# solutions.

### 2. Robot Framework

The Robot Framework's large community of open-source developers has made it arguably the most advanced and stable open-source RPA solution on this list. There are several key benefits for using Robot Framework:

- A consortium of vendors supports the open-source community to update the core product.
- Robot Framework runs on multiple platforms, making it easier for development teams to adopt and implement it.
- The core framework can be extended with an extensive library of plugins.
- The default bots that replicate automation can scale to the needs of an enterprise.

While my teams often use Robot Framework, the tool is complex and may not be the best choice if you are looking to prototype your first RPA solution or if you are new to RPA. That said, experienced RPA developers will appreciate how you can use Robot Framework to manage complex RPA tasks.

### 3. TagUI

TagUI is a multilayered and sophisticated tool with a rich scripting language that lets you complete complex RPA instructions. You develop each set of instructions, referred to as "flows," with TagUI's scripting language and save it in a text file with the extension ".tag." You can then execute each flow using a terminal window/command prompt.

Each flow script can identify the following:

- Instructions to visit a website or open an application
- Where to click on the screen
- Which content to type
- IF and LOOP instructions

The richness of TagUI's scripting language makes it a favorite of our team. We can get the tool up and running quickly, scripts can be shared as .tag files to create a library, and maintaining the library of scripts is easy. TagUI is good for mid-level or advanced teams implementing RPA.

### 4. UI.Vision (Kantu)

UI.Vision (previously known as Kantu), runs either as a standalone client on your desktop or as a plugin in your Web browser. It doesn't require you to learn how to write scripts, since it's driven by a point-and-click interface. That makes UI.Vision an excellent tool to use if you are new to RPA and have limited IT resources.

That said, my teams seldom use UI.Vision. We use it to show the capabilities of RPA in a live demonstration, but the tool lacks the functionality required for more complex scenarios that other tools on this list support—which is the tradeoff you get with a point-and-click interface. More complex controls require scripts and terminal window access that UI.Vision doesn't support.

### 5. Open RPA

While Open RPA offers many customizations and automation capabilities, its main differentiator is its architecture. In a nutshell, Open RPA is a mature tool ready to support and scale for companies of all sizes. It supports many of the features listed with the other tools listed above, including:

- Remote management
- Remote handling of state
- Integration with leading cloud providers
- Scheduling
- Dashboards for analytics

Open RPA is listed here also due to the many active contributors to the project in the open-source community; you can expect to see updates several times per week. My team has limited exposure to working with Open RPA, so we can't vouch for it, but I include it on the list as an alternative solution you might want to try.

## Open-source vs. commercial RPA tools

For many small and mid-sized companies, up-front licensing costs present a barrier to getting an RPA initiative off the ground. In those situations, open source may be your best choice. And in larger companies, open-source tools may serve to fill gaps that commercial products might not fill, such as automating Python.

RPA is an emerging technology that's still in the early adoption phases within many organizations. That's one reason why open-source and commercial tools may serve to complement each other.

There is no one-size-fits-all solution here, so your focus should be on the benefits and value RPA offers and which tools you can use to unlock that value given your budget. As your initiatives mature, your toolbox will probably contain both commercial and open-source elements. But open source is a good way to get started.

## Start simply

Open-source RPA tools come with a significant benefit: Since there are no licensing fees, you use the software without having to go through the process of requesting budget. Just be aware that licensing is often a fraction of the total cost required to run RPA tools.

In fact, open-source tools in general are often more expensive to deploy and can increase the risk.

Furthermore, to scale RPA you need people who are skilled in writing the scripts and managing the environment your bots run in. The need for skilled RPA engineers becomes increasingly crucial as companies come to understand how they can automate other areas of the business and the demand for RPA grows.

As you develop your RPA strategy, start by choosing a simple open-source tool to quickly illustrate RPA's value. Then, as you move from prototype to scaled deployment, you will need something more sophisticated.

What's more, there is no single RPA tool out there that can meet all demands, so it is good to have a blend of commercial and open-source solutions with a team skilled in using the tools to meet all your organization's needs.

## About Matthew David

Matthew David is a Digital Leader at Accenture and a professor at the Academy of Art. Previously global leader of the Kimberly-Clark Mobile Center of Excellence, he was responsible for establishing and enabling an agile and responsive vision and roadmap for the next generation of mobile application capabilities across the enterprise. Matthew is a graduate from Sunderland University, UK, and teaches Masters classes for the Web & New Media program at Academy of Art University. He has published 12 books that have been translated into half a dozen languages on subjects including Flash, HTML5, and Mobile App Design & Development.