---
title: 'Values and politics of Wall Street Journal editorials'
date: 2025-06-25
permalink: /posts/2025/6/wsj_editorials/
summary: 'Blogi | Editorial opinions of Wall Street Journal consider current issues and take positions on them. We use LLM to analyze how opinions are position politically and with respect to values. Accrding to the results, WSJ is clearly a right-wing journal that mostly leans to socially conservative side but occasionally takes socially liberal side.'
tags:
  - politics
  - right-leaning or left-leaning
  - values
  - english
---

Wall Street Journal is a well-regarded American journal. It is often considered to be politically conservative. Here, we analyze how WSJ's editorials position in liberal-conservative axis and on GAL-TAN axis. The results show that WSJ is strongly politically right-wing and mostly socially conservative, even though occasionally WSJ also takes socially liberal side.

![Distribution of WSJ editorials](/images/WSJ/jakauma.png)<br>
_Figure 1. WSJ political viewpoint (x-axis) and values (y-axis)._

1 Background
===

WSJ describes itself as a right-wing entity:

> We speak for free markets and free people, the principles, if you will, marked in the watershed year of 1776 by Thomas Jefferson's Declaration of Independence and Adam Smith's “Wealth of Nations.” So over the past century and into the next, the Journal stands for free trade and sound money; against confiscatory taxation and the ukases of kings and other collectivists; and for individual autonomy against dictators, bullies and even the tempers of momentary majorities. 

Allsides ranks WSJ as a [right leaning media](https://www.allsides.com/news-source/wall-street-journal-opinion).

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

The analysis of this blog is not aimed to be catch-all. There are 100 editorial opinion pieces in the data from May/31/2025 to June/25/2025. A wider database could analyze more throughly, how WSJ positions itself on arvokartta. It would lseo be interesting to see, how the position changes with time.

List of all considered editorial opinions and their assessment is at the end of the blog.

3 Values
===

Editorial opions are clearly TAN: average +3.65 where range is (-10; 10). A typical editorial is even more clearly TAN: median is +5.

![WSJ values](/images/WSJ/arvot.png)<br>
_Figure 2. GAL/TAN axis of WSJ editorials. -10 stands for extremely green, alternative, liberal (GAL), +10 stands for extremely traditional, nationalist, authoritarian (TAN)._

Even though distribution is clearly biased toward TAN, there are GAL viewpoint present in editorials.

4 Politics
===

Editorials are clearly right-wing: average is 6.73 where range is (-10,10).
A typical editorial is also clearly right-wing: median is 7.

![WSJ political](/images/WSJ/poliittinen.png)<br>
_Figure 3. Political bias of WSJ editorials. -10 stands for extremely left-wing, +10 stands for extremely right-wing._

5 Examples
===

5.1 Making a More Beautiful Tax Bill
==

[An editorial about Trump's big, beautiful bill](https://www.wsj.com/opinion/making-a-more-beautiful-tax-bill-f99c655e) is assessed moderately TAN (+2) and very right-wing (+8).

> This is clearly written from a right-wing economic perspective. The article strongly advocates for permanent business tax cuts, criticizes Democrats' potential opposition to these cuts, and frames all policy decisions through a pro-business, supply-side economics lens. It dismisses concerns about deficit costs and advocates for reducing or eliminating tax breaks that benefit workers (tips, overtime) in favor of business expensing provisions. The editorial board's support for the 2017 Trump tax cuts and criticism of Biden-era policies further confirms the right-wing orientation.

> The article focuses primarily on economic growth and business interests without significant emphasis on cultural, environmental, or social justice issues. It doesn't strongly advocate for traditional values or nationalist policies, but its pro-business stance and lack of concern for environmental or social equity considerations places it slightly on the TAN side of the spectrum.

5.2 JD Vance’s False Immigrant Choice
==
[Editorial about foreign students in America](https://www.wsj.com/opinion/jd-vance-immigrants-international-students-visas-donald-trump-b42452ed) is strongly GAL (-6) and clearly right-wing (+4).

> This is a center-right perspective typical of the Wall Street Journal editorial board. While supporting immigration (often associated with the left), it does so primarily through economic and business-oriented arguments about competitiveness, innovation, and human capital. The focus on STEM fields, business needs, and economic prosperity reflects a pro-market, pro-business conservative viewpoint rather than humanitarian or social justice concerns that would characterize a left-wing approach to immigration.

> The article strongly advocates for openness to immigration, particularly skilled immigration and foreign students, which aligns with GAL values of cosmopolitanism and internationalism. It criticizes nationalist restrictions on immigration and emphasizes the benefits of global talent mobility. The piece rejects the 'America First' nationalist approach of Vance and Miller, instead promoting an open, globally-connected vision of American innovation and prosperity.

5.3 Musk trashes the House bill that cuts subsidies for Tesla.
==

[Editorial about Musk's comments on big, beautiful bill](https://www.wsj.com/opinion/elon-musk-house-tax-bill-congress-pork-subsidies-tesla-green-energy-f1834062) is clearly TAN (+5) and clearly right-wing (+7).

> This is clearly written from a right-wing perspective. The editorial strongly supports tax cuts, opposes government spending (especially green subsidies), criticizes the 'climate lobby,' and frames business tax breaks as legitimate while viewing environmental incentives as wasteful. The Wall Street Journal Editorial Board's defense of traditional energy interests and criticism of renewable energy subsidies aligns with conservative economic positions.

> The article takes a moderately TAN position by criticizing green energy subsidies and environmental tax credits as 'pork' and special interest spending. It dismisses climate concerns as 'specious' and mocks the idea that renewable energy is essential for grid reliability. However, it's not extremely TAN as it doesn't explicitly attack environmental values or promote nationalist themes

6 Discussion
===

WSJ is clearly a right-wing journal that mostly leans to socially conservative side but occasionally takes socially liberal side.

Appendix
===

|    | title                                                   | link                                                                                                                                                           |   values |   politics |
|---:|:--------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|---------:|-----------:|
|  0 | Senate Questions for Emil Bove                          | https://www.wsj.com/opinion/emil-bove-senate-questions-third-circuit-eric-adams-danielle-sassoon-b0d10693?mod=editorials_article_pos3                          |       -3 |          3 |
|  1 | Gilead’s HIV Breakthrough                               | https://www.wsj.com/opinion/gileads-hiv-breakthrough-fda-shot-injection-breakthrough-lenacapavir-e9cea9cd?mod=editorials_article_pos2                          |        3 |          7 |
|  2 | Trump and the ‘12-Day War’                              | https://www.wsj.com/opinion/iran-regime-change-donald-trump-qatar-base-israel-ayatollah-ali-khamenei-0d4de9fa?mod=editorials_article_pos1                      |        6 |          8 |
|  3 | TikTok and the Decline of Congress                      | https://www.wsj.com/opinion/donald-trump-tiktok-law-bytedance-china-congress-beabc46a?mod=editorials_article_pos4                                              |        6 |          7 |
|  4 | Trump Meets the Moment on Iran                          | https://www.wsj.com/opinion/trump-meets-the-moment-on-iran-1794ade3?mod=editorials_article_pos5                                                                |        8 |          9 |
|  5 | Frederick W. Smith, 1944-2025                           | https://www.wsj.com/opinion/frederick-w-smith-1944-2025-fedex-founder-entrepreneur-delivery-b81b37a5?mod=editorials_article_pos6                               |        3 |          7 |
|  6 | Iran’s Strait of Hormuz Gambit                          | https://www.wsj.com/opinion/irans-strait-of-hormuz-gambit-oil-middle-east-7df2114a?mod=author_content_page_1_pos_7                                             |        6 |          7 |
|  7 | New York’s Choice: Cuomo or Socialism?                  | https://www.wsj.com/opinion/new-yorks-choice-cuomo-or-socialism-election-mayor-race-vote-mamdani-ede84c75?mod=author_content_page_1_pos_8                      |        6 |          8 |
|  8 | Justice Jackson’s Strange Lament                        | https://www.wsj.com/opinion/ketanji-brown-jackson-dissent-diamond-alternative-energy-v-epa-supreme-court-24ae2bea?mod=author_content_page_1_pos_9              |        6 |          7 |
|  9 | How Iran Is Playing Trump’s Bombing Reprieve            | https://www.wsj.com/opinion/iran-europe-negotiations-donald-trump-abbas-araghchi-866b0d7a?mod=author_content_page_1_pos_10                                     |        6 |          7 |
| 10 | A Bad Time to Stifle Radio Free Iran                    | https://www.wsj.com/opinion/radio-free-europe-iran-kari-lake-usagm-cuts-donald-trump-media-a6f86232?mod=author_content_page_2_pos_1                            |        2 |          6 |
| 11 | A Senate Stablecoin Breakthrough                        | https://www.wsj.com/opinion/senate-stablecoin-regulation-cynthia-lummis-sec-crypto-congress-1d514128?mod=author_content_page_2_pos_2                           |        2 |          6 |
| 12 | MAGA’s Misguided Isolationists                          | https://www.wsj.com/opinion/maga-isolationists-iran-israel-tucker-carlson-donald-trump-republicans-b3ada802?mod=author_content_page_2_pos_3                    |        6 |          8 |
| 13 | The Social Security Iceberg Gets Closer                 | https://www.wsj.com/opinion/social-security-insolvent-2033-medicare-republicans-trustees-9be4c53e?mod=author_content_page_2_pos_4                              |        3 |          7 |
| 14 | America’s Big, Beautiful Land Sale                      | https://www.wsj.com/opinion/federal-land-sale-congress-tax-bill-mike-lee-ryan-zinke-e3e4837f?mod=author_content_page_2_pos_5                                   |        6 |          8 |
| 15 | Exposing ObamaCare Subsidy Fraud                        | https://www.wsj.com/opinion/obamacare-subsidies-health-insurance-fraud-paragon-report-ceb8662b?mod=author_content_page_2_pos_6                                 |        5 |          8 |
| 16 | Good Supreme Court Sense on Trans Hormones              | https://www.wsj.com/opinion/supreme-court-skrmetti-tennessee-transgender-hormone-treatments-e84d97f0?mod=author_content_page_2_pos_7                           |        7 |          8 |
| 17 | The Fed Gets a Tariff Jolt                              | https://www.wsj.com/opinion/federal-open-market-committee-tariffs-interest-rates-dot-plot-donald-trump-jerome-powell-493f2023?mod=author_content_page_2_pos_8  |        2 |          6 |
| 18 | Elon Musk’s Vindication, British Version                | https://www.wsj.com/opinion/elon-musk-u-k-grooming-gangs-audit-louise-casey-keir-starmer-97f5d8b3?mod=author_content_page_2_pos_9                              |        6 |          7 |
| 19 | Another Democrat in Handcuffs                           | https://www.wsj.com/opinion/brad-lander-arrest-ice-new-york-immigration-672cbc2b?mod=author_content_page_2_pos_10                                              |        7 |          8 |
| 20 | Iran Is Trump’s Deterrence Moment                       | https://www.wsj.com/opinion/iran-israel-donald-trump-deterrence-fordow-nuclear-d2ac6ef0?mod=author_content_page_3_pos_1                                        |        8 |          8 |
| 21 | Two Cheers for the Senate Tax Bill                      | https://www.wsj.com/opinion/senate-finance-tax-bill-medicaid-business-gop-e67cbdf5?mod=author_content_page_3_pos_2                                             |        5 |          8 |
| 22 | A New Hope for Middle Eastern Studies                   | https://www.wsj.com/opinion/pepperdine-middle-eastern-studies-program-washington-institute-db914cd9?mod=author_content_page_3_pos_3                            |        5 |          7 |
| 23 | The Oil Price Spike That Wasn’t                         | https://www.wsj.com/opinion/iran-israel-oil-prices-sanctions-trump-white-house-congress-lindsey-graham-c2c4d6b8?mod=author_content_page_3_pos_4                |        6 |          7 |
| 24 | Rand Paul’s Standoff on the Border                      | https://www.wsj.com/opinion/congress-border-spending-homeland-security-rand-paul-donald-trump-stephen-miller-374816b8?mod=author_content_page_3_pos_5          |        3 |          7 |
| 25 | A Legal Ambush Against Dreamers                         | https://www.wsj.com/opinion/texas-dreamers-in-state-tuition-ken-paxton-greg-abbott-department-of-justice-3df53bbd?mod=author_content_page_3_pos_6              |       -6 |          3 |
| 26 | The Fordow Imperative—for Trump and Israel              | https://www.wsj.com/opinion/the-fordow-imperative-for-trump-and-israel-nuclear-enrichment-site-iran-7981fbc0?mod=author_content_page_3_pos_7                   |        7 |          8 |
| 27 | The Art of a Spectrum Deal                              | https://www.wsj.com/opinion/spectrum-deal-congress-ted-cruz-donald-trump-fcc-d30c8d63?mod=author_content_page_3_pos_8                                          |        3 |          7 |
| 28 | Trump’s Good Deportation Exceptions                     | https://www.wsj.com/opinion/trumps-deportation-exceptions-migrant-workers-farms-hotels-870ca047?mod=author_content_page_3_pos_9                                |       -3 |          6 |
| 29 | Canada Shakes Off the Rust on Defense                   | https://www.wsj.com/opinion/canada-defense-spending-mark-carney-military-donald-trump-nato-0f87a14b?mod=author_content_page_3_pos_10                           |        6 |          7 |
| 30 | One Iranian Miscalculation After Another                | https://www.wsj.com/opinion/israel-iran-miscalculation-nuclear-targets-benjamin-netanyahu-e1a3f852?mod=author_content_page_4_pos_1                             |        7 |          8 |
| 31 | Trumping D.C.’s Progressive Pipe Dreams                 | https://www.wsj.com/opinion/washington-d-c-noncitizen-voting-sanctuary-policies-house-democrats-5b109c97?mod=author_content_page_4_pos_2                       |        7 |          8 |
| 32 | Mass Deportation . . . Except at Hotels?                | https://www.wsj.com/opinion/donald-trump-mass-deportation-immigrants-business-vincent-scardina-2c81f53a?mod=author_content_page_4_pos_3                        |       -4 |          3 |
| 33 | Tulsi Gabbard’s Nuclear Strategy                        | https://www.wsj.com/opinion/tulsi-gabbard-nuclear-strategy-atomic-bomb-donald-trump-russia-iran-caa59264?mod=author_content_page_4_pos_4                       |        6 |          7 |
| 34 | Israel’s Nuclear Good Deed Against Iran                 | https://www.wsj.com/opinion/israel-strike-iran-nuclear-attack-netanyahu-trump-c344199b?mod=author_content_page_4_pos_5                                         |        8 |          8 |
| 35 | Don’t Sell Out the Aussies on Aukus                     | https://www.wsj.com/opinion/aukus-australia-submarines-u-s-donald-trump-china-pacific-f9cb0124?mod=author_content_page_4_pos_6                                 |        6 |          7 |
| 36 | Iran’s Latest Nuclear Breakout                          | https://www.wsj.com/opinion/iran-nuclear-non-proliferation-treaty-iaea-uranium-enrichment-trump-administration-5227d152?mod=author_content_page_4_pos_7        |        6 |          7 |
| 37 | The School Choice Boom in Florida                       | https://www.wsj.com/opinion/florida-school-choice-esas-ron-desantis-catholic-schools-0e168a1b?mod=author_content_page_4_pos_8                                  |        6 |          8 |
| 38 | Meet RFK Jr.’s New Vaccine Advisers                     | https://www.wsj.com/opinion/rfk-jr-vaccine-advisory-panel-acip-hhs-martin-kulldorff-james-pagano-vicky-pebsworth-2240dcb0?mod=author_content_page_4_pos_9      |        3 |          5 |
| 39 | U.N. Fudges the Data on West Bank Violence              | https://www.wsj.com/opinion/united-nations-settler-violence-data-israel-west-bank-palestinians-regavim-0186d648?mod=author_content_page_4_pos_10               |        7 |          8 |
| 40 | Trump Has No China Trade Strategy                       | https://www.wsj.com/opinion/china-trade-talks-donald-trump-tariffs-f730f437?mod=author_content_page_5_pos_1                                                    |        2 |          6 |
| 41 | Newsom Rallies the Resistance to Trump                  | https://www.wsj.com/opinion/gavin-newsom-donald-trump-immigration-riots-california-stephen-miller-ice-9d16d88e?mod=author_content_page_5_pos_2                 |        2 |          5 |
| 42 | Chinese Spyware, Only $6.99                             | https://www.wsj.com/opinion/nebraska-lawsuit-china-temu-pinduoduo-mike-hilgers-5767054b?mod=author_content_page_5_pos_3                                        |        6 |          5 |
| 43 | RFK Jr. Conducts His Vaccine Purge                      | https://www.wsj.com/opinion/rfk-jr-vaccine-advisory-committee-purge-acip-hhs-pharma-2249465f?mod=author_content_page_5_pos_4                                   |       -3 |          6 |
| 44 | A Small Fiscal Step for the GOP                         | https://www.wsj.com/opinion/rescissions-vote-gop-congress-spending-cuts-donald-trump-npr-pepfar-98f21e5c?mod=author_content_page_5_pos_5                       |        5 |          8 |
| 45 | Colombia’s Descent Back Into Violence                   | https://www.wsj.com/opinion/miguel-uribe-colombia-murder-attempt-gustavo-petro-6cefb862?mod=author_content_page_5_pos_6                                        |        6 |          7 |
| 46 | New York’s Assisted-Suicide Mistake                     | https://www.wsj.com/opinion/new-york-assisted-suicide-bill-kathy-hochul-amy-paulin-4b41c605?mod=author_content_page_5_pos_7                                    |        7 |          6 |
| 47 | The Housing Lobby’s Tax Boondoggle                      | https://www.wsj.com/opinion/low-income-housing-tax-credit-house-republicans-developers-subsidy-f6d5a1c2?mod=author_content_page_5_pos_8                        |        3 |          7 |
| 48 | Democrats Make Stephen Miller’s Day                     | https://www.wsj.com/opinion/democrats-make-stephen-millers-day-6c430451?mod=author_content_page_5_pos_9                                                        |        7 |          8 |
| 49 | Investigating the Biden Coverup                         | https://www.wsj.com/opinion/investigating-the-biden-cover-up-house-and-doj-probes-b469048c?mod=author_content_page_5_pos_10                                    |        3 |          7 |
| 50 | U.S. Supreme Court 9, Wisconsin Supreme Court 0         | https://www.wsj.com/opinion/u-s-supreme-court-9-wisconsin-supreme-court-0-e08fa87f?mod=author_content_page_6_pos_1                                             |        5 |          7 |
| 51 | The Deportation Wars Begin                              | https://www.wsj.com/opinion/the-deportation-wars-begin-d3cb4f8d?mod=author_content_page_6_pos_2                                                                |        3 |          6 |
| 52 | Making a More Beautiful Tax Bill                        | https://www.wsj.com/opinion/making-a-more-beautiful-tax-bill-f99c655e?mod=author_content_page_6_pos_3                                                          |        2 |          8 |
| 53 | Bondi Bends on Abrego Garcia                            | https://www.wsj.com/opinion/bondi-bends-on-abrego-garcia-788a79bd?mod=author_content_page_6_pos_4                                                              |       -3 |          4 |
| 54 | NATO’s New Military Realism                             | https://www.wsj.com/opinion/natos-new-military-realism-defense-gdp-percent-target-8e3f5532?mod=author_content_page_6_pos_5                                     |        6 |          7 |
| 55 | How to Avoid a ‘Revenge Tax’                            | https://www.wsj.com/opinion/retaliatory-taxes-congress-u-s-businesses-foreign-countries-oecd-janet-yellen-fee5292b?mod=author_content_page_6_pos_6             |        5 |          7 |
| 56 | Signs of a Weaker Labor Market                          | https://www.wsj.com/opinion/signs-of-a-weaker-labor-market-a012f4a1?mod=author_content_page_6_pos_7                                                            |        2 |          6 |
| 57 | JD Vance’s False Immigrant Choice                       | https://www.wsj.com/opinion/jd-vance-immigrants-international-students-visas-donald-trump-b42452ed?mod=author_content_page_6_pos_8                             |       -6 |          4 |
| 58 | An Iran Sanctions Pause Dies a Quiet Death              | https://www.wsj.com/opinion/an-iran-sanctions-pause-dies-a-quiet-death-8d43e4a7?mod=author_content_page_6_pos_9                                                |        6 |          7 |
| 59 | The Mediscare Campaign, CBO Version                     | https://www.wsj.com/opinion/the-mediscare-campaign-cbo-version-d5bb2447?mod=author_content_page_6_pos_10                                                       |        5 |          8 |
| 60 | The Trump-Musk ‘War of the Roses’                       | https://www.wsj.com/opinion/the-trump-musk-war-of-the-roses-543065a0?mod=author_content_page_7_pos_1                                                           |        0 |          3 |
| 61 | Hear, Hear, Sotomayor and Jackson                       | https://www.wsj.com/opinion/hear-hear-sotomayor-and-jackson-7c8ae0d0?mod=author_content_page_7_pos_2                                                           |        3 |          6 |
| 62 | Donald Trump’s New Friend in Germany                    | https://www.wsj.com/opinion/donald-trumps-new-friend-in-germany-e365199c?mod=author_content_page_7_pos_3                                                       |        2 |          6 |
| 63 | Ending a Tax Break for Lawsuits                         | https://www.wsj.com/opinion/lawsuits-tax-break-foreign-investment-firms-thom-tillis-kevin-hern-86b2d7d8?mod=author_content_page_7_pos_4                        |        5 |          8 |
| 64 | Will Trump Take ‘No’ for an Answer?                     | https://www.wsj.com/opinion/donald-trump-russia-iran-negotiations-vladimir-putin-ayatollah-ali-khamenei-999ccacf?mod=author_content_page_7_pos_5               |        5 |          7 |
| 65 | A $4.5 Trillion Tax Increase, or Not?                   | https://www.wsj.com/opinion/congress-tax-bill-cbo-score-deficit-spending-taxes-b4e7dbff?mod=author_content_page_7_pos_6                                        |        3 |          8 |
| 66 | South Korea Takes an Election Left Turn                 | https://www.wsj.com/opinion/south-korea-election-lee-jae-myung-yoon-suk-yeol-e44740ca?mod=author_content_page_7_pos_7                                          |        5 |          7 |
| 67 | When Donald Trump and Sheldon Whitehouse Agree          | https://www.wsj.com/opinion/donald-trump-sheldon-whitehouse-leonard-leo-federalist-society-judges-supreme-court-dce0822e?mod=author_content_page_7_pos_8       |        2 |          6 |
| 68 | Ukraine’s Drone Strike Is a Warning—for the U.S.        | https://www.wsj.com/opinion/ukraine-drone-strike-russia-u-s-homeland-defense-8e2244b2?mod=author_content_page_7_pos_9                                          |        7 |          7 |
| 69 | Whose Pork Do You Mean, Elon?                           | https://www.wsj.com/opinion/elon-musk-house-tax-bill-congress-pork-subsidies-tesla-green-energy-f1834062?mod=author_content_page_7_pos_10                      |        5 |          7 |
| 70 | Paxton, Trump and the Vast Coal Conspiracy              | https://www.wsj.com/opinion/paxton-trump-and-the-vast-coal-conspiracy-33e79dd9?mod=author_content_page_8_pos_1                                                 |       -3 |          7 |
| 71 | The Intifada Comes to Boulder                           | https://www.wsj.com/opinion/boulder-colorado-intifada-antisemitism-mohamed-soliman-576c7462?mod=author_content_page_8_pos_2                                    |        6 |          7 |
| 72 | A Better Way to Make New York Affordable                | https://www.wsj.com/opinion/a-better-way-to-make-new-york-affordable-5f063f01?mod=author_content_page_8_pos_3                                                  |        5 |          7 |
| 73 | Four Justices for AR-15s . . . Next Time                | https://www.wsj.com/opinion/snope-v-brown-supreme-court-ar-15s-second-amendment-brett-kavanaugh-clarence-thomas-db0a1420?mod=author_content_page_8_pos_4       |        5 |          7 |
| 74 | Ukraine Still Isn’t Defeated                            | https://www.wsj.com/opinion/ukraine-drone-strike-suprise-attack-bombers-06955c5e?mod=author_content_page_8_pos_5                                               |        2 |          5 |
| 75 | A ‘Pause’ on New Trump Sanctions Against Iran           | https://www.wsj.com/opinion/-trump-sanctions-iran-pause-karoline-leavitt-de8f5e7c?mod=author_content_page_8_pos_6                                              |        6 |          7 |
| 76 | Wall Street Stages a Weird Tax Bill Freakout            | https://www.wsj.com/opinion/wall-street-stages-a-weird-tax-bill-freakout-35a4f6fe?mod=author_content_page_8_pos_7                                              |        3 |          7 |
| 77 | Iran’s Latest Nuclear Weapons Progress                  | https://www.wsj.com/opinion/irans-latest-nuclear-weapons-progress-trump-deal-enrichment-bomb-95e099ba?mod=author_content_page_8_pos_8                          |        6 |          7 |
| 78 | America’s New Steel Curtain                             | https://www.wsj.com/opinion/americas-new-steel-curtain-tariff-cleveland-cliffs-nippon-3f42801d?mod=author_content_page_8_pos_9                                 |       -3 |          7 |
| 79 | Donald Trump vs. His Own Judges                         | https://www.wsj.com/opinion/donald-trump-vs-his-own-judges-65426dbf?mod=author_content_page_8_pos_10                                                           |       -3 |          6 |
| 80 | France, Yes Even France, Rethinks Low-Emissions Zones   | https://www.wsj.com/opinion/france-yes-even-france-rethinks-low-emissions-zones-f8d868b5?mod=author_content_page_9_pos_1                                       |        6 |          7 |
| 81 | Trump Rides to the Northeast’s Energy Rescue            | https://www.wsj.com/opinion/new-york-pipelines-kathy-hochul-doug-burgum-donald-trump-williams-27b7b260?mod=author_content_page_9_pos_2                         |        6 |          7 |
| 82 | No More Library Police in Texas                         | https://www.wsj.com/opinion/fifth-circuit-library-books-kyle-duncan-first-amendment-2b0f0f50?mod=author_content_page_9_pos_3                                   |        6 |          7 |
| 83 | President Trump Isn’t a Tariff King                     | https://www.wsj.com/opinion/donald-trump-tariffs-ieepa-court-of-international-trade-ruling-08e76022?mod=author_content_page_9_pos_4                            |       -3 |          6 |
| 84 | The Supreme Court Gives Permission to Build Under NEPA  | https://www.wsj.com/opinion/supreme-court-nepa-utah-railroad-environment-surface-transportation-board-brett-kavanaugh-5e937532?mod=author_content_page_9_pos_5 |        6 |          7 |
| 85 | Goodbye to Racial Quotas in Federal Contracts           | https://www.wsj.com/opinion/trump-administration-racial-quotas-dei-disadvantaged-business-enterprise-db3d9478?mod=author_content_page_9_pos_6                  |        6 |          8 |
| 86 | Netanyahu Is Trump’s Leverage With Iran                 | https://www.wsj.com/opinion/iran-donald-trump-negotiations-benjamin-netanyahu-israel-uranium-enrichment-dda2b6b2?mod=author_content_page_9_pos_7               |        6 |          7 |
| 87 | California’s Five-Alarm Pension Fire                    | https://www.wsj.com/opinion/california-firefighter-pensions-unions-jerry-brown-reforms-7feb05d8?mod=author_content_page_9_pos_8                                |        5 |          8 |
| 88 | Big Law Firms 3, Trump 0                                | https://www.wsj.com/opinion/richard-leon-wilmerhale-donald-trump-executive-order-law-firms-perkins-coie-30ad849a?mod=author_content_page_9_pos_9               |       -3 |          4 |
| 89 | GM’s Mary Barra Knows Who’s Boss                        | https://www.wsj.com/opinion/mary-barra-gm-donald-trump-tariffs-automakers-ee644493?mod=author_content_page_9_pos_10                                            |       -2 |          6 |
| 90 | Making New York Less Affordable                         | https://www.wsj.com/opinion/andrew-cuomo-new-york-minimum-wage-eric-adams-zohran-mamdani-mayoral-race-372e724f?mod=author_content_page_10_pos_1                |        5 |          8 |
| 91 | Trump’s Foreign Policy Crossroads                       | https://www.wsj.com/opinion/donald-trump-foreign-policy-russia-china-iran-adversaries-b36e8f80?mod=author_content_page_10_pos_2                                |        6 |          7 |
| 92 | Trump Takes a U.S. Steel Mulligan                       | https://www.wsj.com/opinion/nippon-u-s-steel-deal-japan-donald-trump-united-steelworkers-cleveland-cliffs-6cc798a2?mod=author_content_page_10_pos_3            |       -3 |          7 |
| 93 | Hamas Goes Against the Grain                            | https://www.wsj.com/opinion/hamas-food-aid-gaza-humanitarian-foundation-israel-u-s-cef255a9?mod=author_content_page_10_pos_4                                   |        6 |          7 |
| 94 | ‘There Are CENSORED Genders’                            | https://www.wsj.com/opinion/two-genders-t-shirt-supreme-court-samuel-alito-clarence-thomas-7f3ff50e?mod=author_content_page_10_pos_5                           |        6 |          7 |
| 95 | The Medicaid Scare Campaign                             | https://www.wsj.com/opinion/the-medicaid-scare-campaign-97bc7aa9?mod=author_content_page_10_pos_6                                                              |        3 |          8 |
| 96 | Time for a GOP Senate Revolt on Sanctions Against Putin | https://www.wsj.com/opinion/donald-trump-vladimir-putin-senate-sanctions-bill-lindsey-graham-280e7fbb?mod=author_content_page_10_pos_7                         |        2 |          6 |
| 97 | The New Retirement Age in Denmark Is 70                 | https://www.wsj.com/opinion/the-new-retirement-age-in-denmark-is-70-574b5259?mod=author_content_page_10_pos_8                                                  |        3 |          7 |
| 98 | ‘Stop the Steal’ in U.S. History Class                  | https://www.wsj.com/opinion/oklahoma-social-studies-2020-election-ryan-walters-donald-trump-e6ae3045?mod=author_content_page_10_pos_9                          |       -3 |          3 |
| 99 | Race, Hiring and Chicago’s Mayor                        | https://www.wsj.com/opinion/brandon-johnson-donald-trump-chicago-hiring-dei-investigation-harmeet-dhillon-7d38d7b5?mod=author_content_page_10_pos_10           |        4 |          6 |

