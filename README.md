# Filecoin-Miners-Incubation-Center

## Foreword

So far, there are about  [2700](http://filscan.io/) miners in the Filecoin Network，accounting for more than [6.5EiB](http://filscan.io) storage power. In the meantime, daily growth of storage power between [30-60PiB](http://filscan.io/)，There is a lot of data that is now stored in the Filecoin network. We found most of the storage power is generated by miners in Asia, a few large miners contributed a larger percentage of storage power to the Filecoin network. For a better Filecoin network and resilient ecosystem, improving the storage power proportions from small and medium miners are essential. But due to the cost of investment, software and hardware configuration, and the rapid growth of the Filecoin network, it's not easy to maintain a proper Lucky Value to earn proper reward with providing storage power to the whole network. In the meantime, the slower growth of storage power by small & medium miners also reflects the current Filecoin network needs to be strengthened to better support the small medium miners.

***Distribution of Miners Based on Storage Power***


| Storage Power/PiB | 0 - 0.1 | 0.1 - 0.5 | 0.5 - 1 | 1 - 2 | 2 - 5 | 5 - 10 | 10 - 50 | 50 - 100 | 100 - ♾ |
| ----------------- | ------- | --------- | ------- | ----- | ----- | ------ | ------- | -------- | ------- |
| No. of Miners     | 995     | 500       | 297     | 341   | 319   | 138    | 100     | 9        | 3       |

</br>

## What is Filecoin Miner Incubation Center?

### The progress of Venus

We have supported a distributed mining pool on Filecoin network based on Implementation-[Venus](https://venus.filecoin.io/Home.html), and the distributed mining architecture is designed for small miners. Small miners friendly from a distributed mining pool can be seen in different aspects, including but not limited to:

1. Venus implementation consists of Public and Independent modules which is cost-effective to bring down the overall cost of hardware maintenance and save the time usage when mining on Filecoin network. Thus, it can bring more miners to the Filecoin network with lower barriers to entry.

2. Through independent module(venus-sealer, venus-wallet,etc) management, it's convenient and simple for small miners to manage a single or a few nodes within this system.

3. With the block generation power/right gathered, miners can combine their resources together, in another way, to prevent the situation like no message can be packed for small miners.

4. Stable rewards to small miners from a distributed mining pool is possible, there are multiple plans under design through a better reward distribution mechanism.

</br>

### Filecoin Miner Incubation Center

Miner Incubation Center provides a series of free services to small miners by Venus team supported by resources from public modules，operation and maintenance, technical consultancy, the reason to do so is to make it simple and convenient for small miners to join this network with lower cost and lower barrier to store massdata on the Filecoin Network. 

#### There are 2 tracks in this program:

- Track1: Filecoin Miner Incubation Center Program aims to bring more small miners to the Filecoin network with the financial support from Filecoin Foundation and technical support from Venus Team. 
- Track2: Venus Master Fellowship Program is a sub-project of Filecoin Miner Incubation Center, which aims to incubate teams or individuals capable of providing service of Filecoin distributed mining pool service based on Venus to improve the productivity of miners and the fault tolerance of the Filecoin network. 

</br>

### What do this program provide

Venus team made it possible through [Venus Distributed Ming Pool Architecture](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Overview.md) The incubation center will keep running public modules like（[venus](https://github.com/filecoin-project/venus)、[venus-auth](https://github.com/filecoin-project/venus-auth)、[venus-messager](https://github.com/filecoin-project/venus-messager)、[venus-miner](https://github.com/filecoin-project/venus-miner)、[venus-gateway](https://github.com/ipfs-force-community/venus-gateway)），**miner can just run with** （[venus-sealer](https://github.com/filecoin-project/venus-sealer)、[venus-wallet](https://github.com/filecoin-project/venus-wallet)） and make sure to connect with distributed mining pool then can run with one or a few nodes at the same time.

There may be some issues with joining the incubation center, but we have a Venus team and Venus masters to support you to do so.

Due to the different situation with miners, the time and resources required varies too. We do welcome all miners who are interested in the incubation center to read all the rules and check about the requirements first.

</br>

## Rules and Requirements

### Is it suitable for you? 

![Rules and Requirements](./images/Rules and Requirements.png)

#### Miner Incubation Center Program (Track 1)

The miner incubation center do welcome new or small miners to join immediately, you need to seal at least 64 sectors per day (2TiB）to join this program, when a miner's storage power reached 1PiB or has participated this program over 90days, then the miner has to withdraw from this program, and the others who meet the requirements can be joined.

The first term of Miner Incubation Center started from **2021/07/20 (~25) - 2021/09/30**. If you want to join this program, please register it here [Application Form](http://venusteam.mikecrm.com/1lmpQtj)，please fill as much content as you can so we can review and give feedback to you within a short time. Please be aware, due to the software and hardware varied a lot, we have to learn more about your application before making the right choice. 

##### Benefits to join this program:

1. Saving cost to run with Venus Implementations

Create and run (or switch from Lotus) your node through shared public modules,  those fees will be covered by this program so that’s no cost to build your own public modules like [venus](https://github.com/filecoin-project/venus)、[venus-auth](https://github.com/filecoin-project/venus-auth)、[venus-messager](https://github.com/filecoin-project/venus-messager)、[venus-miner](https://github.com/filecoin-project/venus-miner)、[venus-gateway](https://github.com/ipfs-force-community/venus-gateway). 

2. Technical support to solve your issues

For miners who joined this program, if you faced some issues when running with the program,  we have a Venus team and upcoming Venus masters to support all kinds of issues encountered. Due to the different situation with miners, the time and resources required varies too. 

3. Simple and easy to build your node on Filecoin Network

Miners who joined this program can just run with（[venus-sealer](https://github.com/filecoin-project/venus-sealer)、[venus-wallet](https://github.com/filecoin-project/venus-wallet)）and make sure to connect with a distributed mining pool then can run with one or a few nodes at the same time. it will be easier to build your own node on the largest distributed storage network. Happy Mining!


##### As a miner of Incubation Center:

Candidates should start submitting applications 2 weeks before each milestone, and the application submission period is 1 week.

Our team will start to review the application to select the miners to join this program, and the review period is also 1 week.

#### Venus Master Fellowship Program (Track 2)

The candidate of Venus Master needs to continuously contribute to Filecoin network development with full experience of Filecoin's coding and mining. The selected Master will provide consulting services and technical support to the miners of the incubation center in the related phase to ensure that the miners can continue the growth and help expand the distributed mining pool service in the Filecoin network. 

##### As a Venus Master:

- Provide services to at least 5 miners, such as helping them connect with venus-sealer/wallet to the incubator's mining pool, and provide more storage resources on the Filecoin network.
- Serve at least 1 phase. This process is accompanied by necessary version upgrades and testing.
- During version upgrades or debugging in the miner incubation center, the Master will promptly synchronize the miners in the mining pool to make necessary preparations after receiving the notification.
- The Master will coordinate testing with the Venus Dev team to ensure the quality of service during the version upgrade. 
- Provide feedback on the tools/implementations you are using to ensure the continuous improvement of Venus miners’ experience.
- Provide feedback and suggestions on productivity and load balance, such as energy consumption, cost efficiency, etc.

At the end of each phase, the Master can choose to continue the application of the next phase.

##### Rewards:

- We will provide you with the necessary training to help you use Venus, provide services and in the end, to be a Venus Master.
- At the same time, thanks to the support of the Filecoin Foundation, we have provided Venus Master with a prize pool of 1000+ FILs. The number of the miners you supported and the quality of your service will help you win different amounts of rewards.

### Quota 

Based on the vision of Filecoin, we hope this program can reach miners in different regions. Joining this program will make you one of the Venus community, we do hope you can work with us to test and feedback about the release of Venus versions later on.

In the current situation, the block rewards are generated by its own proportion of storage power in the Filecoin network. We are also working on a better mechanism to distribute rewards within a distributed mining pool, and this mechanism can be decided & improved by your feedback.

#### Quota of track 1: 165+ miners within 1 year. 

| Milestone No. | No. of Miners | Timeline|
| --- | --- | --- |
| 1 | 15 | 2021 July 25st - Sep 31st |
| 2 | 40 | 2021 Oct 1st - Dec 31st |
| 3 | 50 | 2022 Jan 1st - Mar31st |
| 4 | 60 | 2022 Apr 1st - Jun31st |


#### Quota of track 2: 12+Venus Masters within 9months.

| Phase No. | No. of Master | Timeline| Reward / FIL |
| --- | --- | --- | --- | 
| 1 | 3 | 2021 Oct 1st - Dec 31st | 300 |
| 2 | 4 | 2022 Jan 1st - Mar 31st | 400 |
| 3 | 5 | 2022 Apr 1st - Jun 31st | 500 |

*the quota of each track depends on the situation*

</br>

## Things you should know

### Incubation center lower the barrier to entry

The public modules of this program is free for miners who joined this program, you can save at least 1 or more servers' cost to run with independent modules only（servers are required to run with [lotus](https://github.com/filecoin-project/lotus) / [venus](https://github.com/filecoin-project/venus))，details about the accurate number of servers reduced need to be viewed case by case.

#### Resources provided by Incuation Center (Public Modules)：

| Modules                     | CPU  | RAM  | HARD DRIVE | No.                   |
| --------------------------- | ---- | ---- | ---------- | -----------------     |
| venus                       | 32C  | 128G | 4T         | 2（1 for backup）      |
| venus-messager, venus-auth, venus-gateway | 16C  | 32G  | 100G       | 2（1 for backup）      |
| mysql                       | \    | \    | \          | 1（RDS）               |
| venus-miner                 | 32C  | 64G  | 300G       | 1                     |
| *bandwidth*                 |  \   | \    |      \     | *Based on actual needs* |

*According to the actual needs of hardware resources*


#### Resources provided by miner（Independent Module）：

| Module                      | CPU                   | RAM                   | HARD DRIVE            |
| --------------------------- | --------------------- | --------------------- | --------------------- |
| venus-sealer, venus-wallet | Based on actual needs | Based on actual needs | Based on actual needs |

For miners successfully joined this program there will be cost savings to participate in the filecoin network, in the meantime, you will see lower rate of Orplan Block, more stable message signed successfully, higher gas premium and safe wallet to manage your asset.

</br>

### Run with Venus Implementation - User case（based on Venus v0.9.7 releases）

**Deploy Venus Node：** https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/How-To-Deploy-MingPool.md

**Switch from Lotus to Venus：** https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/Venus-replace-lotus.md

</br>

### Call for Your Action

If you are interested in participating in this program, please fill out this application form. We will determine the qualification review of the applicant based on the applicant's technical specifications, location, and the participation in Filecoin.
 
If you have any questions, please leave your comments to Joss-Venus on Filecoin channel of Slack;
 
About [Application Form]() (for miners, and the form for Venus master will be released by the upcoming week), [Incubation Center]()、[Venus Node Deployment](https://github.com/filecoin-project/venus-docs/blob/master/docs/zh/How-To-Deploy-MingPool.md)，if you have any questions, feel free to contact us:

- Slack: [fil-venus](https://filecoinproject.slack.com/archives/CEHHJNJS3)
- Email: [venus@ipfsforce.com](venus@ipfsforce.com)

## Filecoin Community Code of Conduct Applied
We use a common [Code of Conduct](https://github.com/filecoin-project/community/blob/master/CODE_OF_CONDUCT.md#avoid-marketing-or-soliciting) across all of our repos.

## Notice of Risk

Please be noted the Filecoin Miner Incubation center is still in the early stages, public modules from Venus implementation are open sourced under [Apache License 2.0](https://www.apache.org/licenses/LICENSE-2.0.html) and being offered as a non-profit service, in no event and under no legal theory shall Filecoin Miner incubation center be liable to you for any damage resulted from using its services.
