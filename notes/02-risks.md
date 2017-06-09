[← Return to Index](https://github.com/cjmlgrto/fit3140-notes/)

# Risk Management

- **Risk** — a situation involving exposure to danger; a bad thing that may or may not happen
- **Issue** — a situation with certainty

## Risk in Software Projects

- Most IT projects are bug-riddled, over-budget, late or undelivered
- Objective of Software Development is to deliver a working system, on time, for the advertised price
- Risk means exposure to danger of breaching one or more of the following conditions:
	- System not working (or not what was needed)
	- Late delivery or outright cancellation
	- Over-budget (on resources or labour)

## Dealing with Risk

- **Risk Mitigation** — what can be done to make the risk _less likely to occur_ (or if it does occur, _less severe)?
- **Contingency Planning** — if the risks do occur, what can be done to minimise their impact on a software project's objectives?

## What Kinds of Risks Are There?

- Some risks can affect any project, e.g.
	- Loss of team-member, customer pulling out, customer drastically changes requirements
	- Some are rare, such as natural disasters
	- Some are common, such as a bad flu outbreak
- Some are project-specific
	- For example, a third-party library may be unstable or insecure
	- Requirements not properly communicated or understood
	- How do you test an aspect of a project adequately?

## Things Risks can Affect

- Project timeline
- Cost of project
- Fulfillment of requirements (i.e. may change, be misunderstood or just simply infeasible)
- Usefulness to customer (may be wrong about their needs as opposed to their wants)
- Compliance (legal, regulatory requirements, ethics)

## Quantifying and Measuring Risks

- **Impact** — how badly would it affect a project? This can be measured in "points" or on a continuum, ranked by its severity.
- **Likelihood** — how likely is it to happen? This can also be measured on a scale or based on probability.
- **Cost-Benefit Analysis** — finding the maximum amount you should spend on mitigating a risk. The rule of thumb is to find the expected loss by calculating: (probability of risk) × (cost of risk)
	- e.g. If the probability is 2% and the cost is $100,000, then the expected loss is 2% of $100,000 = $2,000 (i.e the max expenditure for mitigating this risk)

## Managing Risks

- In the Waterfall Model (and other similar Software Processes), Risk Management is done during the analysis stage, in which the output includes risk analysis documentation
- Other traditional models call for re-evaluating risks periodically throughout the project

### In Agile Development

- In Agile, ideally, development is risk-focused:
	- Take care of riskiest user-stories first (eliminate risk early as much as possible)
	- Re-evaluate risks at the start of every iteration
	- If new risks discovered during an iteration, discuss with team and add to list if warranted
	- Risks are the responsibility of all team members, not just the project manager

But Agile can still go wrong:

- Its "low-documentation" approach means sometimes a team doesn't plan correctly (i.e. overlook potential problems until too late)
- Need to be good at _estimating_ risks (i.e. how likely and how severe? This is hard to estimate if inexperienced)
- Need to be good at _identifying_ risks (programmers are too optimistic; it's the unknown unknowns that can do serious damage)

## Tools for Managing Risk

- **Risk Matrix** — a 2D-chart used to plot risks on probability versus impact
- **Risk Register** - a comprehensive list of risks, estimations and strategies for dealing with them
- **Risk Burndown Chart**
	- assign values or "points" to each risk (i.e. a sum or product of its likelihood and impact)
	- For each iteration, add up the values of all the risks that haven't been addressed yet, or their new points based on new likelihood and impact
	- Value should decrease as time goes on
	- If it doesn't, improve risk management


