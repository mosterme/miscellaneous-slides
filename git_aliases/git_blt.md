# git blt

![git blt](img/blts.jpg)

<div class="page"/>

# branches

<pre>
<span style="color:green">michael@random</span> <span style="color:orange">~/Projects/yoyodyne</span> <span style="color:teal">(development =)</span>
<span style="color:purple">$</span> git branch

* <span style="color:green">development</span>
  testing
  production
</pre>

&#160;

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git branches

* <span class="yellow">development</span> Prepare Deployment 2023.05 (#95) <span class="green">(2 days ago)</span> <span class="blue">[Michael Ostermeier]</span>
  <span class="orange">testing</span> Merge pull request #96 from origin/development <span class="green">(2 days ago)</span> <span class="blue">[Thomas Müller]</span>
  <span class="orange">production</span> Merge pull request #97 from origin/testing <span class="green">(8 hours ago)</span> <span class="blue">[Thomas Müller]</span>
</pre>

&#160;

<div class="page"/>

# logs

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git log

<span class="orange">commit bbb68f6cf4713272a1acd3a24fc3c72c6c67ad57</span>
Author: Michael Ostermeier <span class="blue">&lt;michael@example.com&gt;</span>
Date: Tue May 30 10:20:40 2023 +0200
Prepare Deployment 2023.05 (#95)
* Added release notes for the 2023.05 deployment.

<span class="orange">commit 119274b431313620c9d9308ede178279fd5aa828</span>
Merge: c815163f 64ade212
Author: Thomas Müller <span class="blue">&lt;thomas@example.com&gt;</span>
Date: Tue May 30 10:05:10 2023 +0200
Merge pull request #94 from origin/issue-548

<span class="orange">commit 64ade21231313620c9d9308ede178279c815163f</span>
Author: Thomas Müller <span class="blue">&lt;thomas@example.com&gt;</span>
Date: Tue May 30 09:45:20 2023 +0200
Add nowrap CSS for Platform.
* Added nowrap CSS for Platform buttons and labels.

<span class="orange">commit fc3c72c6c67ad57bbb68f6cf4713272a1acd3a24</span>
Merge: f3e292bb a66a36b6
Author: Michael Ostermeier <span class="blue">&lt;michael@example.com&gt;</span>
Date: Tue May 22 16:25:35 2023 +0200
Merge pull request #93 from origin/issue-547
:
</pre>

&#160;

<div class="page"/>

# logs

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git log --oneline –n 5

<span class="orange">bbb68f6c</span> (<span class="aqua">HEAD -></span> <span class="lime">development</span>, <span class="red">origin/development</span>) Prepare Deployment 2023.05 (#95)
<span class="orange">119274b4</span> Merge pull request #94 from origin/issue-548
<span class="orange">64ade212</span> (<span class="red">origin/issue-548</span>) Add nowrap CSS for Platform.
<span class="orange">c815163f</span> Merge pull request #93 from origin/issue-547
<span class="orange">a66a36b6</span> (<span class="red">origin/issue-547</span>) Added new News Channel.
</pre>

&#160;

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git logs -n 5

<span class="orange">bbb68f6c</span> (<span class="aqua">HEAD -></span> <span class="lime">development</span>, <span class="red">origin/development</span>) Prepare Deployment 2023.05 (#95) <span class="green">(2 days ago)</span> <span class="blue">[</span>
<span class="orange">119274b4</span> Merge pull request #94 from origin/issue-548 <span class="green">(2 days ago)</span> <span class="blue">[Thomas Müller]</span>
<span class="orange">64ade212</span> (<span class="red">origin/issue-548</span>) Add nowrap CSS for Platform. <span class="green">(2 days ago)</span> <span class="blue">[Thomas Müller]</span>
<span class="orange">c815163f</span> Merge pull request #93 from origin/issue-547 <span class="green">(10 days ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">a66a36b6</span> (<span class="red">origin/issue-547</span>) Added new News Channel. <span class="green">(10 days ago)</span> <span class="blue">[Michael Ostermeier]</span>
</pre>

&#160;

<div class="page"/>

# logs

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git logs readme.md

<span class="orange">09d7cfb2</span> Removed proxy settings from the readme. (#76) <span class="green">(6 weeks ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">06ea4bc8</span> Added gitlab flow diagram to readme. (#29) <span class="green">(4 months ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">b681120e</span> Changed scm link from Bitbucket to GitHub. <span class="green">(7 months ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">2cb53737</span> Removed unused list items from readme. <span class="green">(11 months ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">588df10d</span> Added link to the deployment guide. <span class="green">(1 year, 3 months ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">8a763b51</span> Added link to the Maven POM reference. <span class="green">(1 year, 7 months ago)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">f2c293f0</span> Added readme.md with guides and links. <span class="green">(1 year, 7 months ago)</span> <span class="blue">[Michael Ostermeier]</span>
</pre>

&#160;

<pre>
<span class="purple">$</span> git logs --since="yesterday"                   // Daily Stand-Up Meeting
</pre>

<pre>
<span class="purple">$</span> git logs --since="last friday"                 // Weekly Round Table
</pre>

<pre>
<span class="purple">$</span> git logs --since="two weeks ago"               // Bi-Weekly Catch-Up
</pre>

&#160;

<div class="page"/>

# tags

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git tag

deployment.2023.01
deployment.2023.02
deployment.2023.03
deployment.2023.04
</pre>

&#160;

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git tags

<span class="orange">deployment.2023.01</span> Deployment Production, January 2023 <span class="green">(Thu Jan 26 15:08)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">deployment.2023.02</span> Deployment Production, February 2023 <span class="green">(Thu Mar 9 14:24)</span> <span class="blue">[Michael Ostermeier]</span>
<span class="orange">deployment.2023.03</span> Deployment Production, March 2023 <span class="green">(Tue Mar 28 13:37)</span> <span class="blue">[Thomas Müller]</span>
<span class="orange">deployment.2023.04</span> Deployment Production, April 2023 <span class="green">(Wed May 10 15:43)</span> <span class="blue">[Thomas Müller]</span>
</pre>

&#160;

<div class="page"/>

# intermission

![intermission](img/club.jpg)

<div class="page"/>

# configuration

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git config --get-regexp alias

alias.co checkout
alias.move mv
alias.branches branch --format='%(HEAD) %(if)%(HEAD)%(then)%(color:brightyellow)%(else)%(color:yel
alias.logs log --format='%C(auto)%h%d %s %C(green)(%cr) %C(blue)[%aN]%C(reset)' -n 20
alias.tags tag --format='%(color:yellow)%(refname:short)%(color:reset) %(subject) %(color:green)(%
alias.tree log --graph --format='%C(auto)%h%d %s %C(green)(%cr) %C(blue)[%aN]%C(reset)'
</pre>

&#160;

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git config --edit --global
</pre>

&#160;

<div class="page"/>

# configuration

<pre>
<span class="orange">[alias]</span>
    <span class="teal">co</span> = checkout
    <span class="teal">move</span> = mv
    <span class="teal">branches</span> = branch --format='%(HEAD) %(if)%(HEAD)%(then)%(color:brightyellow)%(else)%(color:yel
    <span class="teal">logs</span> = log --format='%C(auto)%h%d %s %C(green)(%cr) %C(blue)[%aN]%C(reset)' -n 20
    <span class="teal">tags</span> = tag --format='%(color:yellow)%(refname:short)%(color:reset) %(subject) %(color:green)(%
    <span class="teal">tree</span> = log --graph --format='%C(auto)%h%d %s %C(green)(%cr) %C(blue)[%aN]%C(reset)'
    <span class="teal">configure</span> = config --edit --global

<span class="orange">[core]</span>
    <span class="teal">pager</span> = less -F

<span class="orange">[fetch]</span>
    <span class="teal">prune</span> = <span class="red">true</span>

<span class="orange">[user]</span>
    <span class="teal">name</span> = Michael Ostermeier
    <span class="teal">email</span> = michael@example.com
<span class="blue">~</span>
<span class="blue">~</span>
<span class="blue">~</span>
<span class="blue">~</span>
<span class="blue">~</span>
<span class="blue">~</span>
<span class="blue">~</span>
<span class="blue">~</span>
~/.gitconfig [unix] (14:05 05/06/2023)                                                     1,1 All
</pre>

&#160;

<div class="page"/>

# contributors

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git shortlog --no-merges --numbered --summary

   1076 Michael Ostermeier
    269 Gabriel MOUTON
    254 Thomas Müller
    227 Gabriel Mouton
    154 Thomas Mueller
    140 demougab
    102 Nena Zimmermann
     88 DEMUETHO
     57 Hendrik Richter
     21 Stephan Lorenz
     20 Thorsten Ehlers
     10 Alexander Noll
</pre>

&#160;

<div class="page"/>

# contributors

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git contributors

<span class="blue">Michael Ostermeier</span>       <span class="orange">1065 ↑↑</span>      <span class="green">51543 ++</span>      <span class="red">30735 --</span>       4711 🗋🗋
<span class="blue">Gabriel Mouton</span>            <span class="orange">647 ↑↑</span>      <span class="green">72146 ++</span>      <span class="red">30177 --</span>       2772 🗋🗋
<span class="blue">Thomas Müller</span>             <span class="orange">482 ↑↑</span>      <span class="green">22045 ++</span>       <span class="red">9517 --</span>       1177 🗋🗋
<span class="blue">Nena Zimmermann</span>           <span class="orange">102 ↑↑</span>      <span class="green">58622 ++</span>      <span class="red">58750 --</span>        274 🗋🗋
<span class="blue">Hendrik Richter</span>            <span class="orange">57 ↑↑</span>       <span class="green">3176 ++</span>        <span class="red">185 --</span>         56 🗋🗋
<span class="blue">Stephan Lorenz</span>             <span class="orange">21 ↑↑</span>       <span class="green">6275 ++</span>       <span class="red">8609 --</span>        104 🗋🗋
<span class="blue">Thorsten Ehlers</span>            <span class="orange">20 ↑↑</span>        <span class="green">702 ++</span>         <span class="red">99 --</span>         53 🗋🗋
<span class="blue">Alexander Noll</span>             <span class="orange">10 ↑↑</span>        <span class="green">689 ++</span>        <span class="red">510 --</span>         12 🗋🗋
</pre> 

&#160;

<div class="page"/>

# contributors

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> git contributors --since="last year"

<span class="blue">Gabriel Mouton</span>            <span class="orange">128 ↑↑</span>       <span class="green">4070 ++</span>        <span class="red">782 --</span>        311 🗋🗋
<span class="blue">Michael Ostermeier</span>         <span class="orange">69 ↑↑</span>        <span class="green">659 ++</span>        <span class="red">243 --</span>        159 🗋🗋
<span class="blue">Thomas Müller</span>              <span class="orange">42 ↑↑</span>       <span class="green">3099 ++</span>       <span class="red">1849 --</span>        173 🗋🗋
<span class="blue">Stephan Lorenz</span>             <span class="orange">10 ↑↑</span>       <span class="green">5035 ++</span>       <span class="red">8105 --</span>         49 🗋🗋
</pre>

&#160;

<pre>
<span class="green">michael@random</span> <span class="orange">~/Projects/yoyodyne</span> <span class="teal">(development =)</span>
<span class="purple">$</span> cat .mailmap

Gabriel Mouton &lt;gabriel@example.com&gt;
Michael Ostermeier &lt;michael@example.com&gt;
Thomas Müller &lt;thomas@example.com&gt;
</pre>

&#160;

<div class="page"/>

# links

* [Git - git-branch Documentation (git-scm.com)](https://git-scm.com/docs/git-branch)
* [Git - git-log Documentation (git-scm.com)](https://git-scm.com/docs/git-log)
* [Git - git-tag Documentation (git-scm.com)](https://git-scm.com/docs/git-tag)
* [Git - git-for-each-ref Documentation (git-scm.com)](https://git-scm.com/docs/git-for-each-ref)
* [Git - pretty-formats Documentation (git-scm.com)](https://git-scm.com/docs/pretty-formats)
* [Git - mailmap Documentation (git-scm.com)](https://git-scm.com/docs/gitmailmap)<br><br>

* [mosterme / git configuration (GitHub Gist)](https://gist.github.com/mosterme/36e539287442ba2f7f15121124032c13)
* [mosterme / git contributors (GitHub Gist)](https://gist.github.com/mosterme/f44bd5b69736a16fb5a3053fb2e19f0d)<br><br>

* [Write Better Commits, Build Better Projects (GitHub Blog)](https://github.blog/developer-skills/github/write-better-commits-build-better-projects/)

&#160;

<div class="page"/>

# mahlzeit

<img src="img/stulle.jpg" width="1280"/>

<style>
  body {font-size: 125%}
  pre {color: #666}
  .aqua {color: aqua}
  .blue {color: RoyalBlue}
  .green {color: green}
  .lime {color: lime}
  .orange {color: orange}
  .purple {color: purple}
  .red {color: red}
  .teal {color: teal}
  .yellow {color: gold}
</style>