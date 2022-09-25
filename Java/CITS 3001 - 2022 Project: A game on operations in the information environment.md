## Panda学长CS代写
**创始于北美 ｜专注cs全科代写 ｜ 100%原创MOSS查重**

**Panda学长**代写各类程序语言* *: C语言代写, C++代写, 算法作业代写, 数据结构代写, AI/MachineLearning代写, python代写, java代写, matlab代写, 汇编代写, scala代写, SQL/Database代写, racket代写, 安卓/Android代写, IOS/swift代写, racket代写, 网络代写, web代写, OS/操作系统代写, R代写* *

**为什么选择Panda学长CS代写？**

- 我们有经验丰富学历强大的**代写老师**，均毕业于常青藤/清华/北大/北航等顶级CS专业，大部分都是TOP ACMer、LeetCoder, 最快24-48小时即可完成，用技术和耐心帮助客户高效高质量提交作业。
- 我们**价格公道**，绝无高昂的中介费(比中介会便宜很多) 
- 我们的老师都是互相认识的好伙伴，有严格的评价机制，三次差评团队成员就要**强制退出**
- 我们的客服也是由**代写老师轮流担任**，在20分钟内准确高效的评估作业时间和难度，完成后团队有专人负责代码审计。相比于黑中介和个人代写不靠谱，我们团队让您的作业拿到更多分数
- **无限期售后服务**，真正的一站式无忧服务
- 专注留学生编程作业代写,起步于北美，cs业务遍及全球英语国家: [北美CS代写](https://github.com/codedaixie/csdaixie),[美国CS代写](https://github.com/codedaixie/csdaixie),[英国CS代写](https://github.com/codedaixie/csdaixie),[加拿大CS代写](https://github.com/codedaixie/csdaixie),[澳洲CS代写](https://github.com/codedaixie/csdaixie),[新西兰CS代写](https://github.com/codedaixie/csdaixie),[新加坡CS代写](https://github.com/codedaixie/csdaixie),[香港CS代写](https://github.com/codedaixie/csdaixie)

Please feel free to contact us anytime！

**客服24h咨询方式     **微信：cube787**


<img src='https://github.com/codedaixie/csdaixie/blob/main/image/down.png'>
<img src='https://github.com/codedaixie/csdaixie/blob/main/image/logo.png' width='85%'>


### CITS 3001 - 2022

Project: A game on operations in the information environment

Due Date: 13th October
Implementation: Java or Python
Game Scenario
There are four teams involved: Red, Blue, Green and Grey.
The scenario has been deliberately designed to represent the uneven playing field of the
contested environment between the various teams. The scenario highlights the
vulnerabilities of blue team in the contested information environment. The concept of blue
and red teams is prevalent in cybersecurity related serious games or wargames. If you wish
to get some background knowledge about the functioning of teams, you can read this article:
https://csrc.nist.gov/glossary/term/red_team_blue_team_approach. However, this game is
not related to cyber security, rather we are modelling the information environment in a
country.
Red and Blue teams are the major geopolitical players in this fictitious country.
Red team is seeking geopolitical influence over Blue team. Of particular interest to Red team
is influence over Green population and the Government. Blue is seeking to resist the Red
teams growing influence in the country, and promote democratic government in the Green
country.
A key challenge faced by the Blue team, that will become apparent in the exercise, is that
their democratic values are leveraged against them. They are vulnerable to some forms of
manipulation, yet their rules-of-engagement do not allow them to respond in equal measure:
there are key limitations in the ways in which they respond and engage in this unique
battlespace. The Blue team is bound by legal and ethical restraints such as free media,
freedom of expression, freedom of speech.
The Green team lacks a diverse media sector, it is confused and there is a wide range of
foreign news broadcasting agencies Green’s population has subscribed to. The Green
population suffers from poor internet literacy, and the internet literacy can be modelled via
pareto distribution. The government lacks resources to launch a decisive response to foreign
influence operations and a lack of capability to discover, track and disrupt foreign influence
activity.
The Red team, an authoritarian state actor, has a range of instruments, tactics and
techniques in its arsenal to run influence operations. The Green government can block
websites and social media platforms and censor news coverage to its domestic population
whilst maintaining the capability to run sophisticated foreign influence operations through
social media.
The Grey team constitutes foreign actors and their loyalties are not known.
Election day is approaching and the Red team wants to keep people from voting.
Population Model:
An underlying network model that define the probability of nodes interacting with each other.
Majority of the nodes, over 90%, will belong to green team and they depict the population of the country. A small percentage of nodes will be red, blue and grey. At the beginning grey
nodes are not part of the network.
Each green node/agent has an opinion and an uncertainty associated. In every simulation
round nodes will interact with each other and affect each others’ opinions. The more
uncertain an agent is, the more likely their opinion would change. The probability of
interaction is not uniform across all nodes. Some nodes (for instance those in a household),
may have a higher probability to interact.
How teams are going to take turns:
Teams are going to take turns one by one.
1. Red Team: You need to create function where red team (only 1 agent) is able to
interact with all members of the green team. The agent affects the opinions and
uncertainty of the green team during the interaction. The catch is that you need to
select from 5 levels of potent messaging. If the red team decides to disseminate a
potent message, during the interaction round, the uncertainty variable of the red team
will assume a high value. A highly potent message may result in losing followers i.e.,
as compared to the last round fewer green team members will be able to interact with
the red team agent. However, a potent message may decrease the uncertainity of
opinion among people who are already under the influence of the red team (meaning
they are skeptical about casting a vote). You need to come up with intelligent
equations so that red team improves the certainity of opinion in green agents, but at
the same time does not lose too many green agents. Think of it as a media channel
trying to sell their narrative to people. However, if they may big, claim, lie too much,
they might lose some neutral followers which they could indoctrinate with time.
2. Blue Team: Similarly, blue team can push a counter-narrative and interact with green
team members. However, if they invest too much by interacting with a high certainty,
they lose their “energy level”. If they expend all their energy, the game will end. You
need to model this in way that the game keeps going on while the blue team is
changing the opinion of the green team members. Blue team also has an option to let
a grey agent in the green network. That agent can be thought of as a life line, where
blue team gets another chance of interaction without losing “energy”. However, the
grey agent can be a spy from the red team and in that case, there will be a round of
an inorganic misinformation campaign. In simple words, grey spy can push a potent
message, without making the red team lose followers.
