---
title: 'Values and politics of The Economist leaders'
date: 2025-06-30
permalink: /posts/2025/6/the_economist_leaders/
summary: 'Blogi | Leaders of The Economist consider current issues and take positions on them. We use LLM to analyze how opinions are position politically and with respect to values. Accrding to the results, The Economist is clearly a centrist journal that mostly leans to socially liberal side.'
tags:
  - politics
  - right-leaning or left-leaning
  - values
  - english
---

The Economist is a well-known, important British journal concetrating on economic issues. It is often considered to be politically liberal. Here, we analyze how The Economist's leaders position in liberal-conservative axis and on GAL-TAN axis. The results show that The Economist is strongly politically right-wing and mostly socially conservative, even though occasionally WSJ also takes socially liberal side.

![Distribution of The Economist leaders](/images/economist/jakauma.png)<br>
_Figure 1. The Economist political viewpoint (x-axis) and values (y-axis)._

1 Background
===

The Economist is [described](https://en.wikipedia.org/wiki/The_Economist) as 

> "The editorial stance of The Economist primarily revolves around classical, social, and most notably economic liberalism. It has supported radical centrism, favouring policies and governments that maintain centrist politics. The newspaper typically champions economic liberalism, particularly free markets, free trade, free immigration, deregulation, and globalisation."

2 Method
===

A Large Language Model (LLM) can categorize various writing. Recent models have become significantly better at various tasks than previous model. Here we use Anthropic Claude Opus 4 LLM.

Prompts are simple. There are no other prompts used in the analysis.

System prompt:
> You are an AI assistant tasked with analyzing political biases in viewpoints. Your goal is to provide insightful commentary on polical leaning, and on GAL/TAN leaning. Output in JSON format with keys: \“values\” (range (-10,10)), \"politics\" (range (-10,10)), \"explanation values\", and \"explanation politics\".

Analysis prompti:
> Analyze writing. Is it written from a green alternative liberal (GAL) viewpoint or a traditional authoritarion nationalist (TAN) viewpoint? Assess this with range (-10,10). Value -10 means extremely GAL values, value 10 extremely TAN values. Then, is it written from a left-wing or right-wind view point? assess with range (-10,10). Value -10 means an extremely left-wing viewpoint, value 10 extremely a right-wing viewpoint. Answer in JSON form. Encode special chars properly.

The aim of the prompts is to produce a numerical estimate on political leaning and on how socially liberal / socially conservative the editorial is.
Political viewpoint is measured in left-wing / right-wing axis. 

For each analysis, we open a new chat with Claude. In this way, previous chats do not influence the results. Temperature is 0 to keep results as replicable as possible. There is slight change in the results in repetitive runs, even though the prompts are kept the same. The changes are not that large.

The analysis of this blog is not aimed to be catch-all. There are 102 leader opinion pieces in the data from Feb/20/2025 to June/26/2025. 
List of all considered editorial opinions and their assessment is at the end of the blog.

3 Liberal and globalist
===

Editorial opions are clearly GAL, especially globalist and liberal: average -4.13 with range (-10; 10). A typical editorial is also clearly GAL: median is -4.

![The Economist values](/images/economist/values.png)<br>
_Figure 2. GAL/TAN axis of The Economist editorials. -10 stands for extremely green, alternative, liberal (GAL), +10 stands for extremely traditional, nationalist, authoritarian (TAN)._

Even though distribution is clearly biased toward GAL, there are a few TAN viewpoints present in editorials.

4 Centrist leaning left 
===

Leaders are centrist, leaning left: average is -0.53 where range is (-10,10).
A typical editorial is moderately left-wing: median is -2.

![The Economist political](/images/economist/politics.png)<br>
_Figure 3. Political bias of The Economist editorials. -10 stands for extremely left-wing, +10 stands for extremely right-wing._

5 Examples
===

5.1 The world must escape the manufacturing delusion
==
[A leader about various government's fixation on bringing back manufacturing](https://www.economist.com/leaders/2025/04/16/the-lesson-of-birminghams-striking-binmen) is assessed GAL (-6) and right-wing (+3).

| Politics -6 | Values +3 |
| The article takes a moderately right-wing economic stance, advocating for free markets, opposing government subsidies and industrial policy, and warning against state intervention in manufacturing. It criticizes politicians across the spectrum (Trump, Modi, European leaders) for their protectionist policies. The piece champions market efficiency, productivity, and innovation over government-directed industrial planning, which aligns with center-right economic liberalism. | The article strongly advocates for open international trade, global cooperation, and working with allies rather than nationalist protectionism. It criticizes the 'manufacturing delusion' of bringing production home, argues against decoupling from China, and promotes diverse international supply chains. These are classic GAL positions favoring globalization and international integration over nationalist industrial policies. | 


5.2 The lesson of Birmingham’s striking binmen
==
[A leader about Britain's equal-pay laws](https://www.economist.com/leaders/2025/04/16/the-lesson-of-birminghams-striking-binmen) is assessed TAN (+6) and right-wing (+4).

| Politics -6 | Values +3 |
| The article clearly leans right-wing in its economic perspective. It criticizes equal-pay legislation, sympathizes with businesses facing large payouts, and advocates for market-based wage determination. The piece uses typically conservative framing like 'rent-seeking' lawyers and suggests that left-wing councils struggle while Conservative ones succeed through outsourcing. The criticism of EU regulations and the positive framing of Brexit as an opportunity to roll back worker protections further confirms the right-wing orientation." | The article takes a moderately traditional stance by criticizing progressive equal-pay laws that aim to address gender disparities. It frames these laws as 'judicial central planning' and suggests they go against market forces. The piece favors traditional market-based wage determination over interventionist policies designed to promote gender equality. However, it's not extremely TAN as it doesn't invoke nationalist rhetoric or authoritarian themes. | 


5.3 Trump’s incoherent trade policy will do lasting damage
==
[A leader about Trump's trade policy](https://www.economist.com/leaders/2025/04/10/trumps-incoherent-trade-policy-will-do-lasting-damage) is assessed GAL (-6) and left-wing (-4).

| Politics -6 | Values +3 |
| The article leans moderately left in its economic analysis. While it defends free trade (traditionally associated with the right), it does so from a perspective that emphasizes international cooperation, institutional stability, and concern for workers displaced by trade. It criticizes Trump's policies for hurting household incomes and creating market volatility, showing concern for economic inequality. The support for multilateral institutions and criticism of unilateral American actions also reflects a center-left internationalist perspective. | The article strongly embodies GAL values through its defense of free trade, international cooperation, and rules-based global order. It criticizes Trump's nationalist protectionism and 'America First' approach, advocating instead for multilateral trade agreements and international institutions like the WTO. The piece emphasizes the benefits of global economic integration and warns against the dangers of isolationist policies. | 


6 Discussion
===

The Economist is clearly a centrist journal that mostly leans to socially liberal side, that is, a globalist and liberal journal.

Appendix
===

|     | Title                                                                             | URL                                                                                                                          |   values |   politics |
|----:|:----------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|---------:|-----------:|
|   0 | Chinese brands are sweeping the world. Good                                       | https://www.economist.com/leaders/2025/06/26/chinese-brands-are-sweeping-the-world-good                                      |       -3 |          3 |
|   1 | How the defence bonanza will reshape the global economy                           | https://www.economist.com/leaders/2025/06/26/how-the-defence-bonanza-will-reshape-the-global-economy                         |       -3 |          3 |
|   2 | Banning the opposition is no way to revive Bangladesh’s democracy                 | https://www.economist.com/leaders/2025/06/26/banning-the-opposition-is-no-way-to-revive-bangladeshs-democracy                |       -6 |         -2 |
|   3 | How to win peace in the Middle East                                               | https://www.economist.com/leaders/2025/06/26/how-to-win-peace-in-the-middle-east                                             |       -3 |          1 |
|   4 | RFK’s loopy approach to vaccines endangers Americans                              | https://www.economist.com/leaders/2025/06/25/rfks-loopy-approach-to-vaccines-endangers-americans                             |       -6 |         -4 |
|   5 | Trump must offer Iran more than bombs, rage and humiliation                       | https://www.economist.com/leaders/2025/06/22/trump-must-offer-iran-more-than-bombs-rage-and-humiliation                      |       -6 |         -2 |
|   6 | What the “cockroaches” of the ad world teach about dealing with AI                | https://www.economist.com/leaders/2025/06/19/what-the-cockroaches-of-the-ad-world-teach-about-dealing-with-ai                |       -2 |          3 |
|   7 | To keep Russia out and America in, NATO must spend more                           | https://www.economist.com/leaders/2025/06/19/to-keep-russia-out-and-america-in-nato-must-spend-more                          |        2 |          3 |
|   8 | Where will the Iran-Israel war end?                                               | https://www.economist.com/leaders/2025/06/19/where-will-the-iran-israel-war-end                                              |       -3 |         -2 |
|   9 | Why MAGA’s pro-natalist plans are ill-conceived                                   | https://www.economist.com/leaders/2025/06/19/why-magas-pro-natalist-plans-are-ill-conceived                                  |       -6 |         -3 |
|  10 | Japan’s government bonds: this time it won’t end well                             | https://www.economist.com/leaders/2025/06/19/japans-government-bonds-this-time-it-wont-end-well                              |       -2 |          3 |
|  11 | Israel has taken an audacious but terrifying gamble                               | https://www.economist.com/leaders/2025/06/13/israel-has-taken-an-audacious-but-terrifying-gamble                             |       -3 |          1 |
|  12 | How to curb organised crime without shredding civil rights                        | https://www.economist.com/leaders/2025/06/12/how-to-curb-organised-crime-without-shredding-civil-rights                      |       -6 |         -2 |
|  13 | The world must escape the manufacturing delusion                                  | https://www.economist.com/leaders/2025/06/12/the-world-must-escape-the-manufacturing-delusion                                |       -6 |          3 |
|  14 | When a radical performance artist has command of an army                          | https://www.economist.com/leaders/2025/06/12/when-a-radical-performance-artist-has-command-of-an-army                        |       -6 |         -4 |
|  15 | In the age of AI, Apple needs to open up                                          | https://www.economist.com/leaders/2025/06/12/in-the-age-of-ai-apple-needs-to-open-up                                         |       -3 |          3 |
|  16 | Rachel Reeves’s big-government rhetoric is a worrying sign for Britain            | https://www.economist.com/leaders/2025/06/11/rachel-reevess-big-government-rhetoric-is-a-worrying-sign-for-britain           |        2 |          6 |
|  17 | What’s happening in LA could be a template for the Trump administration           | https://www.economist.com/leaders/2025/06/09/whats-happening-in-la-could-be-a-template-for-the-trump-administration          |       -6 |         -5 |
|  18 | Africa’s most admired dictator rolls the dice                                     | https://www.economist.com/leaders/2025/06/05/africas-most-admired-dictator-rolls-the-dice                                    |       -3 |          1 |
|  19 | The stunning decline of the preference for having boys                            | https://www.economist.com/leaders/2025/06/05/the-stunning-decline-of-the-preference-for-having-boys                          |       -6 |         -2 |
|  20 | America’s tax on foreign investors could do more damage than tariffs              | https://www.economist.com/leaders/2025/06/05/americas-tax-on-foreign-investors-could-do-more-damage-than-tariffs             |       -6 |         -3 |
|  21 | Myanmar is a demonstration of Chinese hegemony in action                          | https://www.economist.com/leaders/2025/06/04/myanmar-is-a-demonstration-of-chinese-hegemony-in-action                        |       -6 |         -2 |
|  22 | The West is rethinking how to fight wars                                          | https://www.economist.com/leaders/2025/06/03/the-west-is-rethinking-how-to-fight-wars                                        |        2 |          3 |
|  23 | First he busted gangs. Now Nayib Bukele busts critics                             | https://www.economist.com/leaders/2025/05/29/first-he-busted-gangs-now-nayib-bukele-busts-critics                            |       -7 |         -3 |
|  24 | How Labour should save the NHS                                                    | https://www.economist.com/leaders/2025/05/29/how-labour-should-save-the-nhs                                                  |       -3 |         -4 |
|  25 | American finance, always unique, is now uniquely dangerous                        | https://www.economist.com/leaders/2025/05/29/american-finance-always-unique-is-now-uniquely-dangerous                        |       -3 |         -2 |
|  26 | India needs to turn the air-con on                                                | https://www.economist.com/leaders/2025/05/29/india-needs-to-turn-the-air-con-on                                              |       -5 |          2 |
|  27 | Pausing foreign applications to American universities is a terrible idea          | https://www.economist.com/leaders/2025/05/28/pausing-foreign-applications-to-american-universities-is-a-terrible-idea        |       -7 |         -6 |
|  28 | The plan to protect America by shooting down missiles mid-air                     | https://www.economist.com/leaders/2025/05/22/the-plan-to-protect-america-by-shooting-down-missiles-mid-air                   |       -2 |          0 |
|  29 | The man with a plan for Vietnam                                                   | https://www.economist.com/leaders/2025/05/22/the-man-with-a-plan-for-vietnam                                                 |       -3 |          3 |
|  30 | MAGA’s assault on science is an act of grievous self-harm                         | https://www.economist.com/leaders/2025/05/22/magas-assault-on-science-is-an-act-of-grievous-self-harm                        |       -7 |         -6 |
|  31 | How Poland can keep its place at the heart of Europe                              | https://www.economist.com/leaders/2025/05/22/how-poland-can-keep-its-place-at-the-heart-of-europe                            |       -6 |         -2 |
|  32 | The best part of the UK-EU deal is a system for doing more deals                  | https://www.economist.com/leaders/2025/05/21/the-best-part-of-the-uk-eu-deal-is-a-system-for-doing-more-deals                |       -5 |         -2 |
|  33 | The Senate should vote down Donald Trump’s reckless tax cuts                      | https://www.economist.com/leaders/2025/05/20/congress-should-vote-down-donald-trumps-reckless-tax-cuts                       |       -3 |         -4 |
|  34 | Mexico’s government is throttling the rule of law                                 | https://www.economist.com/leaders/2025/05/15/mexicos-government-is-throttling-the-rule-of-law                                |       -6 |          3 |
|  35 | Europe’s free-speech problem                                                      | https://www.economist.com/leaders/2025/05/15/europes-free-speech-problem                                                     |       -6 |          3 |
|  36 | Crypto has become the ultimate swamp asset                                        | https://www.economist.com/leaders/2025/05/15/crypto-has-become-the-ultimate-swamp-asset                                      |       -3 |         -2 |
|  37 | Is Donald Trump a good dealmaker?                                                 | https://www.economist.com/leaders/2025/05/14/is-donald-trump-a-good-dealmaker                                                |       -3 |         -2 |
|  38 | Stop-gap deals do not mean Donald Trump’s trade war is over                       | https://www.economist.com/leaders/2025/05/14/stop-gap-deals-do-not-mean-donald-trumps-trade-war-is-over                      |       -4 |         -3 |
|  39 | How to handle the AI manager. Advice from our new podcast                         | https://www.economist.com/leaders/2025/05/13/how-to-handle-the-ai-manager-advice-from-our-new-podcast                        |       -3 |         -2 |
|  40 | The war in Gaza must end                                                          | https://www.economist.com/leaders/2025/05/08/the-war-in-gaza-must-end                                                        |       -6 |         -3 |
|  41 | Saudi Arabia is pulling off an astonishing transformation                         | https://www.economist.com/leaders/2025/05/08/saudi-arabia-is-pulling-off-an-astonishing-transformation                       |       -3 |          3 |
|  42 | What Putin wants—and how Europe should thwart him                                 | https://www.economist.com/leaders/2025/05/08/what-putin-wants-and-how-europe-should-thwart-him                               |       -3 |          2 |
|  43 | Donald Trump is right to ditch Joe Biden’s chip-export rules                      | https://www.economist.com/leaders/2025/05/08/donald-trump-is-right-to-ditch-joe-bidens-chip-export-rules                     |       -3 |          3 |
|  44 | Luck stands between de-escalation and disaster for India and Pakistan             | https://www.economist.com/leaders/2025/05/07/luck-stands-between-de-escalation-and-disaster-for-india-and-pakistan           |       -3 |          1 |
|  45 | Donald Trump is right to go after metals in the deep sea                          | https://www.economist.com/leaders/2025/05/01/donald-trump-is-right-to-go-after-metals-in-the-deep-sea                        |        3 |          4 |
|  46 | Britain’s social contract is fraying                                              | https://www.economist.com/leaders/2025/05/01/britains-social-contract-is-fraying                                             |       -3 |         -2 |
|  47 | A superpower crunch over Taiwan is coming                                         | https://www.economist.com/leaders/2025/05/01/a-superpower-crunch-over-taiwan-is-coming                                       |       -3 |          2 |
|  48 | Investors’ risky bet: they can shrug off the trade war                            | https://www.economist.com/leaders/2025/04/30/investors-risky-bet-they-can-shrug-off-the-trade-war                            |       -3 |         -2 |
|  49 | India must prove Pakistan’s complicity in the attack in Kashmir                   | https://www.economist.com/leaders/2025/04/29/india-must-prove-pakistans-complicity-in-the-attack-in-kashmir                  |       -3 |          1 |
|  50 | How to keep AI models on the straight and narrow                                  | https://www.economist.com/leaders/2025/04/24/how-to-keep-ai-models-on-the-straight-and-narrow                                |       -3 |         -1 |
|  51 | Africans need jobs. The rest of the world needs workers                           | https://www.economist.com/leaders/2025/04/24/africans-need-jobs-the-rest-of-the-world-needs-workers                          |       -6 |         -2 |
|  52 | How Canada went from preachy to pragmatic                                         | https://www.economist.com/leaders/2025/04/24/how-canada-went-from-preachy-to-pragmatic                                       |       -3 |          2 |
|  53 | The man Britain cannot ignore                                                     | https://www.economist.com/leaders/2025/04/24/the-man-britain-cannot-ignore                                                   |       -6 |          2 |
|  54 | Trump is a revolutionary. Will he succeed?                                        | https://www.economist.com/leaders/2025/04/24/trump-is-a-revolutionary-will-he-succeed                                        |       -7 |         -6 |
|  55 | President Trump’s attacks on the Fed are not over                                 | https://www.economist.com/leaders/2025/04/23/president-trumps-attacks-on-the-fed-are-not-over                                |       -3 |         -2 |
|  56 | Brazil’s Supreme Court is on trial                                                | https://www.economist.com/leaders/2025/04/16/brazils-supreme-court-is-on-trial                                               |       -3 |          2 |
|  57 | Don’t overlook the many benefits of plastics                                      | https://www.economist.com/leaders/2025/04/16/dont-overlook-the-many-benefits-of-plastics                                     |        3 |          2 |
|  58 | The lesson of Birmingham’s striking binmen                                        | https://www.economist.com/leaders/2025/04/16/the-lesson-of-birminghams-striking-binmen                                       |        4 |          6 |
|  59 | How a dollar crisis would unfold                                                  | https://www.economist.com/leaders/2025/04/16/how-a-dollar-crisis-would-unfold                                                |       -6 |         -4 |
|  60 | Zuckerberg on trial: why Meta deserves to win                                     | https://www.economist.com/leaders/2025/04/15/zuckerberg-on-trial-why-meta-deserves-to-win                                    |       -3 |          4 |
|  61 | In its pursuit of a policy, Donald Trump’s government is content to destroy a man | https://www.economist.com/leaders/2025/04/15/in-its-pursuit-of-a-policy-donald-trumps-government-is-content-to-destroy-a-man |       -7 |         -6 |
|  62 | How AI could help the climate                                                     | https://www.economist.com/leaders/2025/04/10/how-ai-could-help-the-climate                                                   |       -6 |         -2 |
|  63 | Donald Trump’s oddly sensible move: seeking a deal with Iran                      | https://www.economist.com/leaders/2025/04/10/donald-trumps-oddly-sensible-move-seeking-a-deal-with-iran                      |       -3 |         -2 |
|  64 | MAGA’s remaking of universities could have dire consequences                      | https://www.economist.com/leaders/2025/04/10/magas-remaking-of-universities-could-have-dire-consequences                     |       -7 |         -3 |
|  65 | Trump’s incoherent trade policy will do lasting damage                            | https://www.economist.com/leaders/2025/04/10/trumps-incoherent-trade-policy-will-do-lasting-damage                           |       -6 |         -4 |
|  66 | Europe should buy from Ukraine’s defence industry                                 | https://www.economist.com/leaders/2025/04/09/europe-should-buy-from-ukraines-defence-industry                                |       -3 |          2 |
|  67 | Donald Trump was right. Daylight Saving Time needs to go                          | https://www.economist.com/leaders/2025/04/03/donald-trump-was-right-daylight-saving-time-needs-to-go                         |       -2 |          0 |
|  68 | Why the IMF should bail out a serial deadbeat                                     | https://www.economist.com/leaders/2025/04/03/why-the-imf-should-bail-out-a-serial-deadbeat                                   |       -3 |          6 |
|  69 | How America could end up making China great again                                 | https://www.economist.com/leaders/2025/04/03/how-america-could-end-up-making-china-great-again                               |       -6 |         -3 |
|  70 | President Trump’s mindless tariffs will cause economic havoc                      | https://www.economist.com/leaders/2025/04/03/president-trumps-mindless-tariffs-will-cause-economic-havoc                     |       -7 |         -3 |
|  71 | Lift sanctions to give Syria a chance of rebuilding                               | https://www.economist.com/leaders/2025/04/02/lift-sanctions-to-give-syria-a-chance-of-rebuilding                             |       -6 |         -2 |
|  72 | Why Marine Le Pen should be allowed to run for president                          | https://www.economist.com/leaders/2025/04/01/why-marine-le-pen-should-be-allowed-to-run-for-president                        |       -3 |          0 |
|  73 | First, jab more babies                                                            | https://www.economist.com/leaders/2025/03/27/first-jab-more-babies                                                           |       -6 |         -3 |
|  74 | Israel’s expansionism is a danger to others—and itself                            | https://www.economist.com/leaders/2025/03/27/israels-expansionism-is-a-danger-to-others-and-itself                           |       -6 |         -3 |
|  75 | Is Elon Musk remaking government or breaking it?                                  | https://www.economist.com/leaders/2025/03/27/is-elon-musk-remaking-government-or-breaking-it                                 |       -6 |         -3 |
|  76 | The unpredictability of Trump’s tariffs will increase the pain                    | https://www.economist.com/leaders/2025/03/27/the-unpredictability-of-trumps-tariffs-will-increase-the-pain                   |       -6 |         -3 |
|  77 | Labour can still rescue Britain’s growth prospects                                | https://www.economist.com/leaders/2025/03/26/labour-can-still-rescue-britains-growth-prospects                               |       -3 |          2 |
|  78 | President Recep Tayyip Erdogan is throttling Turkey’s democracy                   | https://www.economist.com/leaders/2025/03/25/president-recep-tayyip-erdogan-is-throttling-turkeys-democracy                  |       -7 |         -2 |
|  79 | The judges Trump scorns should stand their ground                                 | https://www.economist.com/leaders/2025/03/20/the-judges-trump-scorns-should-stand-their-ground                               |       -6 |         -3 |
|  80 | How to enhance humans                                                             | https://www.economist.com/leaders/2025/03/20/how-to-enhance-humans                                                           |       -4 |          2 |
|  81 | If you can’t find a place to rent, blame the government                           | https://www.economist.com/leaders/2025/03/20/if-you-cant-find-a-place-to-rent-blame-the-government                           |       -3 |          6 |
|  82 | The trap Vladimir Putin has set for Donald Trump                                  | https://www.economist.com/leaders/2025/03/19/the-trap-vladimir-putin-has-set-for-donald-trump                                |       -6 |         -3 |
|  83 | Britain at last takes aim at worklessness                                         | https://www.economist.com/leaders/2025/03/18/britain-at-last-takes-aim-at-worklessness                                       |       -2 |          3 |
|  84 | Time is running out for Syria’s president                                         | https://www.economist.com/leaders/2025/03/13/time-is-running-out-for-syrias-president                                        |       -4 |         -2 |
|  85 | With Manus, AI experimentation has burst into the open                            | https://www.economist.com/leaders/2025/03/13/with-manus-ai-experimentation-has-burst-into-the-open                           |       -3 |          1 |
|  86 | The new economics of immigration                                                  | https://www.economist.com/leaders/2025/03/13/the-new-economics-of-immigration                                                |       -4 |          2 |
|  87 | America’s bullied allies need to toughen up                                       | https://www.economist.com/leaders/2025/03/13/americas-bullied-allies-need-to-toughen-up                                      |       -6 |         -3 |
|  88 | Will Vladimir Putin really agree to stop his killing machine?                     | https://www.economist.com/leaders/2025/03/12/will-vladimir-putin-really-agree-to-stop-his-killing-machine                    |       -5 |         -2 |
|  89 | Trump’s erratic policy is harming the reputation of American assets               | https://www.economist.com/leaders/2025/03/12/trumps-erratic-policy-is-harming-the-reputation-of-american-assets              |       -6 |         -4 |
|  90 | Lifting sanctions on Syria seems mad, until you consider the alternative          | https://www.economist.com/leaders/2025/03/06/lifting-sanctions-on-syria-seems-mad-until-you-consider-the-alternative         |       -4 |         -2 |
|  91 | Britain’s leader has found purpose abroad. He needs it at home too                | https://www.economist.com/leaders/2025/03/06/britains-leader-has-found-purpose-abroad-he-needs-it-at-home-too                |       -3 |          3 |
|  92 | The demise of foreign aid offers an opportunity                                   | https://www.economist.com/leaders/2025/03/06/the-demise-of-foreign-aid-offers-an-opportunity                                 |       -3 |          3 |
|  93 | Donald Trump’s economic delusions are already hurting America                     | https://www.economist.com/leaders/2025/03/06/donald-trumps-economic-delusions-are-already-hurting-america                    |       -6 |         -4 |
|  94 | A fantastic start for Friedrich Merz                                              | https://www.economist.com/leaders/2025/03/05/a-fantastic-start-for-friedrich-merz                                            |       -3 |          3 |
|  95 | The lesson from Trump’s Ukrainian weapons freeze                                  | https://www.economist.com/leaders/2025/03/04/the-lesson-from-trumps-ukrainian-weapons-embargo                                |       -6 |         -3 |
|  96 | Western leaders must seize the moment to make Europe safe                         | https://www.economist.com/leaders/2025/03/01/western-leaders-must-seize-the-moment-to-make-europe-safe                       |       -6 |         -2 |
|  97 | Prabowo Subianto takes a chainsaw to Indonesia’s budget                           | https://www.economist.com/leaders/2025/02/27/prabowo-subianto-takes-a-chainsaw-to-indonesias-budget                          |       -6 |         -3 |
|  98 | Inheriting is becoming nearly as important as working                             | https://www.economist.com/leaders/2025/02/27/inheriting-is-becoming-nearly-as-important-as-working                           |       -4 |         -3 |
|  99 | Donald Trump has begun a mafia-like struggle for global power                     | https://www.economist.com/leaders/2025/02/27/donald-trump-has-begun-a-mafia-like-struggle-for-global-power                   |       -7 |         -3 |
| 100 | CRISPR technologies hold enormous promise for farming and medicine                | https://www.economist.com/leaders/2025/02/26/crispr-technologies-hold-enormous-promise-for-farming-and-medicine              |       -6 |          3 |
| 101 | Germany’s election victor must ditch its debt rules—immediately                   | https://www.economist.com/leaders/2025/02/24/germanys-election-victor-must-ditch-its-debt-rules-immediately                  |       -4 |         -2 |