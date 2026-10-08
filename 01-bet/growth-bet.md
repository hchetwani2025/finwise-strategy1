# The Bet · FinWise

> Module 1 · Ignite a PLG Motion. The growth hypothesis and where you're betting, plus the growth-loop visualization.

## Growth hypothesis

### Exercise 1 — first hunch (before the data)

**Hypothesis:** I think FinWise's biggest problem is that trial users do not reach the product's value before the trial ends, so paid ads fill the top of the funnel with people who leave.

**Evidence from the scenario:**
- Only 2% of trials convert to paid. 98 of every 100 trial users leave.
- 60% of paid customers churn within a year. The people who do pay also do not find lasting value.
- More ad spend no longer drives growth. The limit is not the number of people who try FinWise; it is what happens after they try it.

**First bet:** Test a guided first-week path (import data → build a first model) for new trial users, because the feature a user must reach to see value is the cheapest point to fix.

| | |
|---|---|
| **IF** | we show new trial users a guided path that ends with a first cash-flow model built from their own imported data |
| **THEN** | the share of trial users who complete a model in week 1 will increase by 10 to 15 points |
| **BECAUSE** | users who never see their own numbers inside FinWise have no reason to pay |
| **MEASURED WITH** | A/B test over 4 weeks; week-1 model completion (primary); day-1 drop-off (guardrail) |

### Exercise 2 — what the data showed

Funnel totals, Oct 2023 – Oct 2024 (13 months):

| Stage | Count | Rate from prior stage |
|---|---|---|
| Website visits | 94,558 | — |
| Trials started | 6,424 | 6.8% |
| Paid conversions | 128 | 2.0% |

**Biggest drop-off:** trial → paid. FinWise loses 98% of trial users at this step (vs. 93% at visit → trial). Funnel stage: **Activation** (the trial users never reach the point where the product earns a payment; the loss shows up in Revenue).

**Pattern that surprised me most:** feature use rose a lot, but conversion did not move at all.
- Users who built a model rose from 10.8% (Nov 2023) to 58.1% (Sep 2024), more than 5×.
- Users who imported data rose from about 31% (Jan–Mar 2024) to about 45% (Jul–Oct 2024).
- Trial → paid stayed between 1.87% and 2.08% in **every** month (standard deviation 0.06 points).
- Paid count follows trial count almost exactly (correlation 0.99). Paid = about 2% of trials, no matter what users do in the trial.

**Other patterns:**
- Visits do not predict trials (correlation 0.09). June 2024 had the most visits (9,426) and the fewest trials (321, a 3.4% rate). July 2024 had the fewest visits (5,466) and the most efficient month (11.2%). More traffic gives a lower visit → trial rate (correlation −0.64), which fits "more ad spend no longer works."
- Users either have many short sessions or few long ones (sessions per user vs. session length: −0.81).
- Data caveats: revenue is exactly $78,125 × paid customers every month, so the revenue column adds no new signal. "Churned (1yr)" totals 317 against 128 new paid customers, so it must count the older customer base, not these cohorts.

**Did the data confirm or challenge my hypothesis? — Challenged it.**

My Exercise 1 bet assumed that more feature use in the trial would raise conversion. The data says FinWise already ran that experiment without meaning to: model use went up 5× and conversion stayed flat at 2%. Pushing more users into the same features is unlikely to change the outcome. The real limit is that paid customers are a fixed 2% slice of trials, and trials come only from ads that no longer scale. FinWise needs a new source of trials that costs nothing per user and that brings in users who are more likely to stay.

## The bet

**Growth loop to test first: Collaboration.**

Small-business finance is rarely a one-person job: the owner works with an accountant or bookkeeper. A Collaboration loop turns each trial into a path to a second user (who makes the account harder to leave) and, through the accountant, to new businesses (which gives FinWise trials that do not come from ads).

### Formalized hypothesis

- **PROBLEM (X):** FinWise's biggest growth problem is that new paid customers are a fixed 2% of trials, and trials depend on paid ads that no longer scale.
- **BECAUSE (Y):** each trial is a single-user, single-business account. Nothing in the product brings in a second user or a second business, so growth stops when ad spend stops working.
- **EXPERIMENT (Z):** the highest-leverage experiment I'd run first is an "invite your accountant" step at the end of data import, with a free accountant seat that lets them review and comment on the books.

| | |
|---|---|
| **IF** | we ask trial users to invite their accountant or bookkeeper right after they import data, and give that person a free seat |
| **THEN** | trial accounts with an invited collaborator will convert at 3% or more (vs. 2% baseline), and accountant-sourced trials will reach 5% of all new trials within 8 weeks |
| **BECAUSE** | an owner with a second person working inside the account has more reason to pay and stay, and an accountant serves many businesses that can each start a trial |
| **MEASURED WITH** | 50/50 split of new trials over 8 weeks. **Primary (leading):** share of trials that send an invite, and share of invites accepted within 7 days. **Secondary:** trials started by accountants, per active accountant. **Guardrail:** import completion rate and day-1 drop-off must not fall. |

**Why the primary metric is a leading signal, not conversion:** FinWise gets about 494 trials a month. To detect a change from 2% to 3% conversion with normal confidence (95%, 80% power), the test needs about 3,800 trial users in each group. That is about 15 months of traffic. A 2- or 8-week test cannot measure conversion directly, so the test measures the behavior that should cause conversion, then follows the cohorts to paid status over the next quarters.

### What I am deliberately not doing

- **Not putting more money into paid ads.** The data shows visits do not predict trials.
- **Not running another in-trial feature push.** Model use rose 5× with no change in conversion.
- **Not changing price or the reverse-trial paywall yet.** It may matter, but it splits effort from the loop, and pricing tests at this volume are just as slow to read.
- **Not starting a churn program for existing customers.** The 60% churn is real, but the loop should help it as a side effect (multi-user accounts), and I want to see that before I spend on it separately.

## Growth loop

![FinWise collaboration growth loop](finwise-growth-loop.png)

- **Trigger:** a small-business owner starts a FinWise trial and imports their books.
- **Stage 1:** the owner invites their accountant or bookkeeper (free seat) to review the books.
- **Stage 2:** the accountant works inside FinWise: reviews, comments, closes the month. The owner now depends on FinWise to work with their accountant.
- **Stage 3:** the accountant sees that FinWise saves time and adds more of their small-business clients.
- **Outcome:** multi-user accounts convert and stay at a higher rate; each new client the accountant adds starts a new trial, so the loop restarts with a larger base.

**Loop health metric:** new trials sourced per active accountant per month. If this number is above zero and rising, the loop compounds; if accountants join but add no clients, the loop is only a retention feature, not a growth loop.
