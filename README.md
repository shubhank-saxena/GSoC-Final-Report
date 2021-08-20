
<p align="center">
<img src="https://github.com/shubhank-saxena/GSoC-Final-Report/blob/master/src/banner.jpeg">
</p>

Organisation: [GFOSS Open Technology Alliance](https://github.com/eellak/) <br/>
Project: 
[MediaCMS](https://github.com/mediacms-io/mediacms) - modern, fully featured video and media CMS <br/>
Mentor: [Markos Gogoulos](https://github.com/mgogoulos)

## 📙 Abstract
My proposal was selected for `MediaCMS - modern, fully featured video and media CMS`under `GFOSS Open Technologies Alliance`. <br/>
`MediaCMS` is a modern, fully featured open-source video and media CMS. It is developed to meet the needs of modern web platforms for viewing and sharing media. It can be used to build a small to medium video and media portal within minutes.<br/>
It is built mostly using the modern stack `Django + React, Celery` and includes a `REST API`. `MediaCMS` is a very useful project empowering communities around the globe to host their own media and content management system. It also helps educational institutes to manage their media and course curriculum by supporting various media formats like Video, Audio, PDF. Docs, etc.

## 📝 About the project(s)
(PS: here’s [the link](https://github.com/shubhank-saxena/gsoc-proposals/blob/master/GFOSS_MediaCMS_Proposal.pdf) to my GSoC proposal, if you’re interested!) <br/>
The aim of my project(s) was to improve the existing features of MediaCMS and add some new broad features.<br/>
The theme and goal was to improve the user experience as well as deployment experience from the admin side. The following are some of the projects I undertook during my GSoC - 

### Internationalization
Internationalization describes the process of designing products to meet the needs of users in many countries or designing them so they can be easily modified, to achieve this goal.<br/> 
The endgoal of this project is to make sure that the project is as inclusive as possible for our evergrowing users from different geographies. This project's integration will open doors for us to make sure that further translations are easy and thus the community can support us for the same! <br/>
This was achieved by using [react-i18next](https://react.i18next.com/) <br/><br/>
Link to the PR - [https://github.com/mediacms-io/mediacms/pull/251](https://github.com/mediacms-io/mediacms/pull/251) <br/><br/>

<img src="https://github.com/shubhank-saxena/GSoC-Final-Report/blob/master/src/i18n.gif">
<p align="center"> Glimpse of internationalization</p>

### Segregation of Dev and Prod envs
For every open-source project to be successful and grow at a great pace, it is essential that the project should be more developer friendly. <br/>
Thus it was necessary to segregate the development and production environments so that developers can run the project locally with bare-minimum configuration. The following was achieved by - 
- Creation of new dockerfile for dev.
- Creation of new docker-compose for dev.
- Seperating all python dependencies into two files, ie, `requirements.txt` and `requirements-dev.txt`
<br/><br/>

Link to PR - [https://github.com/mediacms-io/mediacms/pull/218](https://github.com/mediaccms-io/mediacms/pull/218)

### Addition of UI based tests
The MediaCMS is not completely a single page application (soon going to be converted!). So there was a need to test django form components. <br/>
I used [Selenium](https://django-selenium.readthedocs.io/en/latest/) as a tool to test UI components. The big challenge was to integrate everything as a docker runtime, so for that I used [docker-selenium](https://github.com/SeleniumHQ/docker-selenium).<br/><br/>
Link to PR - [https://github.com/mediacms-io/mediacms/pull/236](https://github.com/mediacms-io/mediacms/pull/236)

### Imrpovement of code quality via Linting
For the project to be at par with the accepted conventions of underlying language, it is essential that the codebase is properly linted. <br/>
To maintain this, I added [pre-commit](https://pre-commit.com/) and created a Github Action based CI out of it. So everytime someone has to commit code to the repo, their Pull Request will go through lint checks and they will have to respect lint standards set by the project!<br/>
Link to PR - [https://github.com/mediacms-io/mediacms/pull/140](https://github.com/mediacms-io/mediacms/pull/140)

### CLI tool for interacting with MediaCMS APIs
For admins, managing, uploading files can be a tedious task. And when the interface is GUI based with single input as a option, it becomes more tedious. <br/>
The idea behind this tool is to act like a CLI based wrapper around already existing MediaCMS. This can be super helpful for :
- Schedule file uploads.
- Checking various info and metadata about files for reference.
- Bulk uploading files to server.
<br/>
Link to PR - [https://github.com/mediacms-io/mediacms/pull/273](https://github.com/mediacms-io/mediacms/pull/273)
<br/><br/>
<img src="https://github.com/shubhank-saxena/GSoC-Final-Report/blob/master/src/cli.gif">
<p align="center"> Glimpse of CLI tool</p>

## :computer: Pull Request Statistics
A list of all the pull requests that I created during GSoC coding period:
<table>
<thead>
<tr>
<th>Status</th>
<th>PR Title</th>
<th>Diff</th>
</tr>
</thead>
<tbody>
<tr>
<td>✅</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/140">Add pre-commit</a></td>
<td><font color ='green'>+53 <font color ='red'>−1</td>
</tr>
<tr>
<td>✅</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/218">Segregation of Dev and Prod envs</a></td>
<td><font color ='green'>+171 <font color ='red'>−42</td>
</tr>
<tr>
<td>🚧</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/236">UI tests via selenium</a></td>
<td><font color ='green'>+115 <font color ='red'>−1</td>
</tr>
<tr>
<td>🚧</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/251">i18n changes</a></td>
<td><font color ='green'>+183 <font color ='red'>−1249</td>
</tr>
<tr>
<td>🚧</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/256">Addition of JS Lint</a></td>
<td><font color ='green'>+33,471 <font color ='red'>−31,220</td>
</tr>
<tr>
<td>🚧</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/272">Test Coverage reporting</a></td>
<td><font color ='green'>+33 <font color ='red'>−2</td>
</tr>
<tr>
<td>🚧</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/273">CLI API Tool</a></td>
<td><font color ='green'>+134 <font color ='red'>−3</td>
</tr>
<tr>
<td>🚧</td>
<td><a href = "https://github.com/mediacms-io/mediacms/pull/274">Pre-commit upgrade</a></td>
<td><font color ='green'>+189 <font color ='red'>−196</td>
</tr>
</tbody>
</table>

## :star: Acknowledgements
From working on personal projects, to working on a production grade application, the Google Summer of Code was such an eventful journey. Learning by doing is the best possible experience that anyone can have, and I am grateful of having the opportunity to be part of such an amazing program :heart: <br/><br/>
Thank you [Markos](https://github.com/mgogoulos) for being such an amazing mentor. I am so glad to have you as my guide at every step of my GSoC journey. It was your guidance that helped me grow a lot as a developer.<br/><br/>
Special thanks to [Philip](https://github.com/swiftugandan) for helping me understand the deployment process of the entire project and [Yiannis](https://github.com/styiannis) for helping me out with the frontend components! <br/><br/>
To the reader who is reading this, thank you for making it so far. I know I speak for every developer out there, when I say <u>it means a lot</u> when you choose to look at someone's journey or their work product; it could as well be a tiny website, or it could be as big as designing a complete library.<br/><br/>
![Team MediaCMS](https://github.com/shubhank-saxena/GSoC-Final-Report/blob/master/src/team.png)
<p align="center"> Team MediaCMS</p>

## What's next?
I am grateful that I was able to work on this amazing project and I will continue to work further. Open Source is all about contributing as a community and should not be restricted to standard Open Source programs.<br/>
[MediaCMS Repo](https://github.com/mediacms-io/mediacms) is an amazing beginner friendly project and I encourage anyone interested, should contribute. Do reach out to me for any queries.
<br/>
<h4 align="left">Thank you! You can connect with me at:</h4>
<p align="center">
<a href="https://twitter.com/19_saxena"><img src="https://github.com/aritraroy/social-icons/blob/master/twitter-icon.png?raw=true" width="60"></a>
<a href="https://www.linkedin.com/in/shubhank-saxena"><img src="https://github.com/aritraroy/social-icons/blob/master/linkedin-icon.png?raw=true" width="60"></a>
<a href="https://facebook.com/shubhank.saxena2"><img src="https://github.com/aritraroy/social-icons/blob/master/facebook-icon.png?raw=true" width="60"></a>
<a href="https://shubhank.codes"><img src="https://github.com/shubhank-saxena/GSoC-Final-Report/blob/master/src/icons8-globe-96.png?raw=true" width="60"></a>
<a href="https://blog.shubhank.codes"><img src="https://github.com/shubhank-saxena/GSoC-Final-Report/blob/master/src/icons8-blog-256.png?raw=true" width="60"></a>
</p>
