	


# COVID-19 in data (in the US):  How bad is it?

In this note, I work to synthesize a few different kinds of epidemiological results into aggregate "what might the (range of plausible projections for the) risk be to a given person in a given age range?" estimates.  In particular, the result most often reported seems the case fatality rate (CFR), as estimated in some specific place and time.  This captures the fatality rate for people who (a) have already contracted COVID-19, and (b) have been recognized as such. If we wish to extend the CFR to some notion of risk to an arbitrary resident, those last two points make a big difference.  In this note I factor in estimates of what fraction people who are infected with the virus (SARS-CoV-2) go unnoticed in CFR estimates, and what fraction are likely to become infected at all.  There are multiple studies on each of these factors, and individual studies often present a range of estimated or project values.  I have taken into account high and low estimates for each factor (though sometimes excluding a few that look like outliers) and considered various combinations of each.  The result is a range of "reasonable" risk estimates that are consistent with the current research that I am aware of.

## Notes

First, I am *not* an epidemiologist, microbiologist, or other expert in the field.  These are "back of the envelope" calculations using other people's data.  All the raw numbers come from reputable sources:  official reports and "real" scientific papers, though a some are preprints due to the compressed timescale involved in researching a new and rapidly-evolving epidemic. The interpretation and the way they're combined, however, is my quick-and-dirty estimation, not solid science.  It is possible, for example, that different studies are based on fundamentally incompatible assumptions or definitions, and an estimate that blithely combines the two doesn't make a lot of sense.

Second, I've been sitting on a not-quite-finished version of this post for a little over a week while doing other things.  That means that new discoveries and new work from the last week or so are not incorporated.  This reflects an early-March 2020 understanding.

## Case Fatality Rate

The first statistic of interest in the case fatality rate (CFR).  That is, *if* a person is infected by SARS-CoV-2 (that is, the virus that causes COVID-19), whether they become symptomatic or not, what is the probability that they will die[1, 17]?

That sounds easy to calculate, right?  It's just # of deaths / # of infected people.  In principle, it's not very hard to determine the # of deaths, because deaths are not subtle and are already recorded and tracked.  Certainly there are some false positives and false negatives, but it's probably not wildly off.  It's the denominator that's the bitch here.  It's relatively easy to count "people who sought medical care in a hospital and were identified as having COVID-19 and that was reported to public health officials" but that's not really the question.  Between that number and the gross number of people who contracted the virus lie:  Cases recognized but not reported; cases seen in the medical system but not recognized; cases in which the sick person did not seek medical assistance at all; and cases in which the person is not noticeably symptomatic, even to themselves.  Each of those is generally multiplicatively larger than the category before it, so that there can be orders of magnitude difference between the number of identified cases and the total number of infected people.  Estimating this part - how many more unrecognized cases are there for each one that's identified - is the biggest source of uncertainty and divergence.  Note also that CFR is _not_ a fixed truth about the virus[1 again].  It's a measure of how the particular people infected to date have fared in their specific situations. See also [11] for other challenges, especially the temporal aspects:  It can take 2 to 3 weeks from when a person is identifiably infected and when they recover or die, meaning that the data about people contracting the disease is weeks out of sync with data about people's outcomes.  This can be addressed by looking at safely-old data, but looking three weeks in the past is less than ideal for an epidemic that has changed a lot in that interval.

The latest "authoritative" estimate of CFR that I've seen is from a WHO briefing[2], which suggests about 3.4% _of reported cases_.  I believe I've seen estimates as low as 0.4% and as high as 4%, but those aren't coming up when I look right now.  At this point, the largest and best epidemiological studies are coming out of China (naturally) with largest that I'm aware of estimating 2.3% fatality (again, out of detected / reported cases)[4].  A recent follow-up study compared results in Italy and China and found very close agreement between data in both countries, including the Italy CFR coming in at about 2% as well[3].

It seems reasonable to say at this point that the _aggregate_ CFR is somewhere in the 1.5% to 3.5% range, for people who are sick enough to seek medical help and are recognized, and/or are successfully recognized at some kind of screening.

## (Non-) Detection

Because I'm going to be talking about the spread of the virus later, I really want to look at the overall risk to anybody who is infected by it, whether or not they're sick enough, and in the right ways, to be recognized.  This paper[7] discusses the challenge of detection in the specific context of screening travelers.  This report [8] estimates that between 63% and 73% of the cases *exported* from China have been undetected, which is a decent proxy for the detection rate in general. [9] estimates the non-detection rate in Italy at 72% (confidence interval 61% to 79%). The other estimates I've found suggest that between 50% and 90% of cases are *not* detected, which in turn suggests that the infected-individual fatality is rate is between 10% and 50% of the reported fatality rates.  

Sooo, combining the two steps gives us a range of values for this "true CFR":

|                        |        | Low CFR est. (1.5%) | High CFR est. (3.5%) |
|------------------------|--------|-------------------|--------------------|
| Low non-detection est. | (50%)  |    0.75%          |       1.75%        |
| Middle[10]             | (72%)  |    0.42%          |       0.98%        |
| High non-detection     | (90%)  |    0.15%          |       0.35%        |

As a generic averaged human, your chances of dying *if you contract the virus* are between 1/666 and 1/57, depending. Most likely between 0.42% (1/240) and 0.98% (1/102). Now, nobody is a generic average, and the COVID-19 fatality statistics are very much differentiated by age (and a few other risk factors).  

Here are age-specific estimated CFRs for the epidemic in China[4].   

<!-- | As reported                 Adjusted for estimated non-detection rates -->
<!-- |-------------                 ------------------------------------------ -->

| &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; **As reported** &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; | &nbsp; &nbsp; &nbsp; &nbsp; &nbsp; **Adjusted for estimated non-detection rates** &nbsp;&nbsp;&nbsp;&nbsp; |

| Age (yr) | Est'd CFR(%)    | Low (50%) | Mid (72%) | High(90%)  |
|-----     | --------:       |-------    |-------    |-------     |
| 0–9      |  −              | -         |    -      |    -       |
| 10–19    | 0.2             | 0.1%      |  0.05%    |  0.02%     |
| 20–29    | 0.2             | 0.1%      |  0.05%    |  0.02%     |
| 30–39    | 0.2             | 0.1%      |  0.05%    |  0.02%     |
| 40–49    | 0.4			 | 0.2%	     |  0.11%	 |  0.04%     |
| 50–59    | 1.3		     | 0.65%	 |  0.36%	 |  0.13%     |
| 60–69    | 3.6			 | 1.8%	     |  1.01%	 |  0.36%     |
| 70–79    | 8.0			 | 4%	     |  2.34%	 |  0.8%      |
| ≥80      | 20.3		     | 10.15%	 |  5.68%	 |  2.03%     |

There's nothing radically shocking here:  If you're a teenager or young adult, in the best case your risk is 0.02%, or 1/5000.  If you're over 80, in the worst case your risk is about 10%, or 1/10.  And all the other cases are in between.  The age-specific CFRs could be split into low, high, and middle estimates just as we did with the overall CFR, but I haven't seen enough research on that to make guesses.  And that table doesn't need to be three times as large and ten times as confusing.

Taking the liberty of cherry-picking what seem like "pretty reasonable" middle values of the various ranges, I get to something like this:

| Who      | Low-end CFR    | High-end CFR   |
|---       |-----------     |------------    |
| Everyone lumped together   |      0.35%    |  1%  (I left off the lowest and highest values from our CFR x Detection square) |
| 0- 9 yr   |       0	   |    0            |
| 10-39 yr  |  0.02%	   |    0.1%         |
| 40-49 yr  |  0.04%	   |    0.2%         |
| 50-59 yr  |  0.13%	   |    0.36%        |
| 60-69 yr  |  0.36%	   |    1.8%         |
| 70-79 yr  |  0.8%		   |    4%           |
| ≥80 yr    |  2.03%       |   10.15%        |

And that's what I've got.  That's my range of estimates for "*if* you get the virus, how likely is it to be fatal?"  And that needs a bunch of caveats.  Like, the probability of detection isn't necessarily the same across age groups, for example.

## Fraction of the population likely to be infected

The other key question is: How likely are you to get it at all?

If the epidemic is successfully contained, you could be very unlikely to contract the virus.  I'm going to go out on a limb and say that seems pretty unlikely[12]:  There are confirmed cases on every continent except Antarctica, with community transmission and increasing numbers almost everywhere.  From what I've heard, China and South Korea have implemented robust -- some would say draconian -- surveillance and isolation measures, but nobody else is really on the ball.  That's not an insult, it's just that spreading is what viruses do, all of humanity is one big buffet of susceptible individuals, and fully shutting down transmission is a high bar.  So, assume the cat's out the bag. The virus is likely to spread until there's nowhere left to go.  As far as I know, fighting off the infection once confers immunity against future reinfection, so the pool of "infectible" people shrinks as infection progresses.  That effectively reduces the reproduction rate because more and more of the people who might otherwise catch the infection are immune.  That means the epidemic can die out before *everyone* is infected because there aren't enough susceptible people left to sustain it.  The estimates I've seen suggest that for SARS-CoV-2, that threshold is around 50% [13], with some projections ranging from about 30% to 70%. If we apply these to our previous estimates, we get something like this:

| Who           |Low-end CFR * 30%   | High-end CFR * 70%    |  Age-Specific Death Rate |
| ---           |-----------------   |------------------     |  ----------------------- |
| Everyone lumped  together  |  0.10%  | 0.7%          | all    0.87%                   |
| 0- 9 yr       |     0		 |   0                     | 1-4:   0.024%,   5-9: 0.012%   |
| 10-39 yr	    | 0.006%	 |   0.07%                 | 15-24: 0.074%, 25-34: 0.133%   |
| 40-49 yr	    | 0.012%	 |   0.14%                 | 35-44: 0.19%                   |
| 50-59 yr      | 0.039%	 |   0.25%                 | 45-54: 0.40%,  55-64: 0.89%    |
| 60-69 yr	    | 0.11%		 |   1.26%                 | 54-64: 0.89%,  65-74: 1.8%     |
| 70-79 yr	    | 0.24%		 |   2.8%                  | 75-84: 4.5%                    |
| ≥80 yr		| 0.61%		 |   7.1%                  | ≥85:   13.6%                   |

The age-specific death rate, included for comparison, is the fraction of the population in each age group who die in any given year. The label "all" refers to the population wide crude death rate. (These numbers are for 2017 [14,15].) In the worst case, across age ranges the risk of dying from COVID-19 is in the same ballpark as the combined risk of dying of anything else, though still smaller.  In the best case, it's about 1/10th the risk of everything else.  Looking at the aggregate fatality rate estimates, the best case corresponds to approximately 330 thousand deaths in the United States, and the worst case corresponds to approximately 2.32 million.

I meant to write a conclusion, but I can't:  What those numbers mean to me might be very different from what they mean to you.


## Notes

1. Sort of.  CFR is an aggregate, retrospective statistic about the infections and deaths that have happened to date.  Since any given person who gets infected may be in a very different situation than the previous infected people who went into the CFR, the new person might have a correspondingly different personal prognosis.  But it's probably an OK first approximation for the population as a whole.

2. "WHO Director-General's opening remarks at the media briefing on COVID-19 - 3 March 2020" Mar. 03 2020, available at 	     https://www.who.int/dg/speeches/detail/who-director-general-s-opening-remarks-at-the-media-briefing-on-covid-19---3-march-2020

3. Porcheddu, R., C. Serra, D. Kelvin, N. Kelvin, and S. Rubino. “Similarity in Case Fatality Rates (CFR) of COVID-19/SARS-COV-2 in Italy and China”. The Journal of Infection in Developing Countries, Vol. 14, no. 02, Feb. 2020, pp. 125-8, doi:10.3855/jidc.12600.

4. The Novel Coronavirus Pneumonia Emergency Response Epidemiology Team. "The Epidemiological Characteristics of an Outbreak of 2019 Novel Coronavirus Diseases (COVID-19) — China, 2020." China CDC Weekly Vol. 2, no. x, Feb. 14 2020, available at https://github.com/cmrivers/ncov/blob/master/COVID-19.pdf


5. https://www.who.int/emergencies/diseases/novel-coronavirus-2019/global-research-on-novel-coronavirus-2019-ncov


6. Shi Zhao, Salihu S. Musa,Qianying Lin, et. al. "Estimating the Unreported Number of Novel Coronavirus (2019-nCoV) Cases in China in the First Half of January 2020: A Data-Driven Modelling Analysis of the Early Outbreak" J. Clin. Med. 2020, 9(2), 388; available at  https://doi.org/10.3390/jcm9020388

7. Katelyn Gostic, Ana CR Gomez, Riley O Mummah, Adam J Kucharski, James, and Lloyd-Smith eLife "Estimated effectiveness of symptom and risk screening to prevent the spread of COVID-19" EPIDEMIOLOGY AND GLOBAL HEALTH 2020;9:e55570  DOI: 10.7554/eLife.55570

8. Sangeeta Bhatia, Natsuko Imai, Gina Cuomo-Dannenburg, et. al. "Report 6: Relative sensitivity of international surveillance." WHO Collaborating Centre for Infectious Disease Modelling, MRC Centre for Global Infectious Disease Analysis, Abdul Latif Jameel Institute for Disease and Emergency Analytics (J-IDEA), Imperial College London.  Feb. or maybe Mar. 2020. Available at https://www.imperial.ac.uk/media/imperial-college/medicine/sph/ide/gida-fellowships/Imperial-College---COVID-19---Relative-Sensitivity-International-Cases.pdf

9. Ashleigh Tuite, Victoria Ng, Erin Rees, and David Fisman. "Estimation of COVID-19 outbreak size in Italy based on international case exportations" Mar. 6 2020. Preprint at medRxiv doi: https://doi.org/10.1101/2020.03.02.20030049 available at https://www.medrxiv.org/content/10.1101/2020.03.02.20030049v1

10. Independent studies on China, a portfolio of countries receiving travelers from China, and Italy have all come up with 72% plus or minus a couple percent, so I'm calling this the most likely, but that's still a personal judgment call.

11. Ana Sandoiu, fact-checked by Isabel Godfrey. "Why are COVID-19 death rates so hard to calculate? Experts weigh in" Mar. 5 2020. Medical News Today, on-line article.  Available at https://www.medicalnewstoday.com/articles/why-are-covid-19-death-rates-so-hard-to-calculate-experts-weigh-in#Death-rate-may-only-be-known-at-the-end

12. Hamblin, James. “You’re Likely to Get the Coronavirus.” The Atlantic, February 24, 2020. https://www.theatlantic.com/health/archive/2020/02/covid-vaccine/607000/.

13. Flahault, A. (2020). Has China faced only a herald wave of SARS-CoV-2? The Lancet, 0(0). https://doi.org/10.1016/S0140-6736(20)30521-3

14. https://www.cdc.gov/nchs/products/databriefs/db328.htm, https://www.cdc.gov/nchs/data/databriefs/db328_tables-508.pdf#5

15. Kochanek KD, Murphy SL, Xu JQ, Arias E. "Deaths: Final data for 2017." National Vital
Statistics Reports; vol 68 no 9. Hyattsville, MD: National Center for Health Statistics. 2019. Available at: https://www.cdc.gov/nchs/data/nvsr/nvsr68/nvsr68_09-508.pdf

16. I see CFR used to refer to the fatality rate for either the population that's explicitly identified as infected, or the entire population of infected people, whether they're recognized or not.  That is, some empirical work attempts to estimate and compensate for the undetected population, while some seems to (knowingly) pass them over, leaving it to the reader to take this into account.  My usage is inconsistent, but all the work I reference is in the second category. 

# Revisited, 1 Year On

## Age-Specfic Infection Fatality Rates

| Who       | "My" estimates, March 2020   | Brazeau[^1] estimates 
|---        |-----------       |------------- 
| Aggregate |   0.35% --   1%  | 1.06% (0.73% -- 1.65%)
| 0- 9 yr   |      0  --   0   | 0.005% (0.00% -- 0.045%)
| 10-39 yr  |  0.02%  -- 0.1%  | 0.04% (0.003% -- 0.44%)
| 40-49 yr  |  0.04%  -- 0.2%  | 0.19% (0.025% -- 1.62%)
| 50-59 yr  |  0.13%  -- 0.36% | 0.46% (0.075% -- 2.9%)
| 60-69 yr  |  0.36%  -- 1.8%  | 1.14% (0.26% -- 5.0%)
| 70-79 yr  |  0.8%	  -- 4%    | 2.78% (0.92% -- 8.5%)
| ≥80 yr    |  2.03%  -- 10.15% | 9.9% (5.2% -- 19.3%)


"Brazeau" estimate column refers to the "IFR (%) with Seroreversion (95% PI)" column of Table 2 "Pooled-Estimates of the Infection Fatality Rate" from [^1].  "Aggregate" here is the "High-Income Country (HIC)" overall. The report uses five-year age brackets; the values given here for 10+ year brackets are simple (unweighed) averages of the corresponding rows from the report.  That's absolutely *not* statistically valid, but it's not terrible for a rough summary if one doesn't abuse it too much.

| Who      | Levin[^2] estimates
|--        |-------
|  0-34 yr | 0.004% (0.003% -- 0.005%)
| 35-44 yr | 0.068% (0.058% – 0.078%)
| 45-54 yr | 0.23% (0.20% – 0.26%)
| 55-64 yr | 0.75% (0.66% – 0.87%)
| 65-74 yr | 2.5% (2.1% – 3.0%)
| 75-84 yr | 8.5% (6.9% – 10.4%)
| ≥85 yr   | 28.3% (21.8% – 36.6%)

Levin et al [^2] did a different meta-analysis, and chose to give their results by age brackets that perversely fail to align with the ones I used previously, so I them here separately.  The estimates shown here are those in Table 3 "Age-specific fatality rates for COVID-19 infections vs. acci- dental deaths (%)."

## U.S. Mortality

At the time of writing (February 17, 2021), the CDC estimates that there have been 486,466 deaths in the united[^3] and project a total of 530,000 to 559,000 as of March 13 2021[^4].

## Notes

[^1]: Brazeau, N, R Verity, S Jenks, H Fu, C Whittaker, P Winskill, I Dorigatti, et al. “COVID-19 Infection Fatality Ratio: Estimates from Seroprevalence.” Imperial College London, October 29, 2020. https://doi.org/10.25561/83545.


[^2]: Levin, Andrew T., William P. Hanage, Nana Owusu-Boaitey, Kensington B. Cochran, Seamus P. Walsh, and Gideon Meyerowitz-Katz. “Assessing the Age Specificity of Infection Fatality Rates for COVID-19: Systematic Review, Meta-Analysis, and Public Policy Implications.” European Journal of Epidemiology 35, no. 12 (December 1, 2020): 1123–38. https://doi.org/10.1007/s10654-020-00698-1.

[^3]: Centers for Disease Control and Prevention (CDC). “COVID Data Tracker (United States COVID-19 Cases and Deaths by State),” March 28, 2020. https://covid.cdc.gov/covid-data-tracker.


[^4]: Centers for Disease Control and Prevention (CDC). “Observed and Forecasted New and Total Reported COVID-19 Deaths as of February 15, 2021,” February 17, 2021. https://www.cdc.gov/coronavirus/2019-ncov/covid-data/forecasting-us.html.
