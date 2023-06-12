# Example 1 - Direct marketing of term deposits - Part 1

## Introduction

There are two main approaches for companies to promote products and/or services: through mass campaigns, targeting general indiscriminate public, or through **direct marketing**, targeting a specific set of contacts. Nowadays, in a global competitive world, positive responses to mass campaigns are typically very low. Alternatively, direct marketing focus on targets that assumably will be keener to that specific product/service, making these campaigns more attractive, because of their efficiency. But the increasingly vast number of marketing campaigns has reduced their effect on the general public. Furthermore, economical pressures and competition has led marketing managers to invest on direct campaigns with a strict and rigorous selection of contacts.

Due to the internal competition and the current financial crisis, there are huge pressures for European banks to increase their financial assets. One strategy is to offer attractive **long-term deposit** applications with good interest rates, in particular by using direct marketing campaigns.

A Portuguese institution has been offering term deposits to its clients for the past two years, but in a way that the board finds disorganized and inefficient. It looks as if too many contacts were made, for the subscriptions obtained.

The bank has been using its own contact-center to carry out direct marketing campaigns. The telephone was the dominant marketing channel, although sometimes with an auxiliary use of the Internet online banking channel (*e.g*. by showing information to a specific targeted client). Furthermore, each campaign was managed in an integrated fashion and the results for all channels were outputted together.

The manager in charge of organizing the next campaign is expected to optimize the effort. His objective is to find a **predictive model**, based on data of the preceding campaign, which can explain the success of a contact, *i.e*. if the client subscribes the deposit. Such model can increase the campaign's efficiency by identifying the main characteristics that affect success, helping in a better management of the available resources (eg human effort, phone calls and time) and the selection of a high quality and affordable set of potential clients. To be useful for the direct campaign, a predictive model should allow to reduce the number of calls in a relevant way without loosing a relevant number of subscribers.

## The data set

The data for this example come from the previous phone campaign of the bank, which involved a total of 45,211 contacts. During that campaign, an attractive long-term deposit application, with good interest rates, was offered. The contacts led to 5,289 subscriptions, a 11.7% **conversion rate**.

The data set combines demographic data with data about the interaction of the client and the bank. The original variables have been transformed into **dummy variables** (1/0) so they can be directly entered in an equation:

* Age in years (`age`).

* Type of job (`job`). The values are 'admin', 'blue-collar', 'entrepreneur', 'housemaid', 'management', 'retired', 'self-employed', 'student', 'technician', 'unknown' and 'unemployed'. Converted to twelve dummies.

* Marital status (`marital`). The values are 'married', 'divorced' and 'single'. Converted to three dummies.

* Education level (`education`). The values are 'unknown', 'secondary', 'primary' and 'tertiary'. Converted to four dummies.

* Has credit in default (`default`)? The values are 'yes' and 'no'. Converted to a dummy (1 for 'yes' and 0 for 'no').

* Average yearly balance in euros (`balance`).

* Has housing loan? (`housing`). The values are 'yes' and 'no'. Converted to a dummy (1 for 'yes' and 0 for 'no').

* Has personal loan? (`loan`). The values are 'yes' and 'no'. Converted to a dummy (1 for 'yes' and 0 for 'no').

* Usual communication channel (`contact`). The values are 'unknown', 'telephone' and 'cellular'. Converted to three dummies.

* Duration of last contact before the campaign in seconds (`duration`). 

* Number of days passed by after the client was last contacted from a previous campaign (`pdays`). The entry is -1 when the client has not been previously contacted.

* Number of contacts performed before this campaign and for this client (`previous`).

* Outcome of the previous marketing campaign (`poutcome`). The values are 'unknown', 'other', 'failure' and 'success'. Converted to four dummies.

* Has the client subscribed a term deposit (`deposit`)? The values are 'yes' and 'no'.

Source: S Moro, P Cortez & P Rita (2014), A data-driven approach to predict the success of bank telemarketing, *Decision Support Systems* **62**, 22-31.

## Questions

Q1. Develop a **logistic regression model** to predict the response to the campaign (`deposit`) from the other variables.

Q2. Use your model to obtain a **predictive score** for every client. How is the distribution of the scores? Is it different for the subscribers and the non-subscribers?

Q3. Based on your model, if we set a target of 4,000 subscriptions, how many calls would we need, to hit the target?

Q4. If we set a budget 10,000 calls, how will we select the clients to be called? How many subscriptions will we get?

Q5. Suppose that you decide to use your model as suggested in question Q4, but calling 20% of your clients. How would you validate your model for that application, based on a **train/test split**?

