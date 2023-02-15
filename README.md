![](https://github.com/lunardao/dao/blob/main/moon3.gif)

# LunarDAO Architecture

**THIS DOCUMENT IS A PROPOSAL AND REFERENCE FOR THE COMMUNITY FEEDBACK AND [DISCUSSION](https://forum.lunardao.net/t/tokenomics-lunar-vox/89/45)!**

**Resources & References**

* [LunarDAO architecture discussion](https://forum.lunardao.net/t/tokenomics-lunar-vox/89/45)
* [MolochDAO V2](https://github.com/MolochVentures/moloch)
* [Metacartel Ventures whitepaper](https://github.com/metacartel/MCV/blob/master/MCV-Whitepaper.md#asset-management)
* [Moloch Baal - V3](https://github.com/Moloch-Mystics/Baal)
* [Summon a DAO](https://summon.daohaus.fun/)
* [LunarDAO tokenomics V1](https://wiki.lunardao.net/tokens.html) - this model will NOT be used, however this report refers to it in some parts
* [LunarDAO Manifesto](https://wiki.lunardao.net/)
* [LunarDAO: Why are we anonymous](https://lunardao.net/why-anon.html)
* [LunarDAO Multi-sig Anouncement](https://lunardao.net/sentinel-committee-announcement.html)


## General

[LunarDAO](https://lunardao.net/) aims to function as an **INVESTMENT FUND INTO PRIVACY PROJECTS & ANONYMITY TOOLING**, a squad wealth based DAO spreading [Lunarpunk narrative](https://wiki.lunardao.net/) & philosophy and creating possibilities for education by building [research](https://wiki.lunardao.net/anoma.html)/[wiki](https://wiki.lunardao.net/intro.html) and support [educational](https://wiki.lunardao.net/academy_intro.html) processes where people master the skills in the field and bring value back to the ecosystem.

Based on the discussions with the allies & the community, the most feasible way for the LunarDAO architecture to meet its aim, seems to be MolochDAO V3. The contracts have much more optionality on both the initial setup and throughout the DAO life time in comparison to Moloch V2. V3 is also easier to set up and launch, possibly using existing UI and implement changes on the fly, in more democratic manner (based on community discussions and squad vote).

- Multisig Gnosis Safe and Moloch v3 on chain execution are compatible -> the DAO can be setup on top of the [Gnosis safe multisig](https://lunardao.net/sentinel-committee-announcement.html). Start with the trust (and more secure) setup and plan a roadmap milestone to discuss, propose (LIP) and vote on a multi-sig removal in a forseeable future -> full trustless setup.
- RageQuit is included in this design.
- Setup minimum retention 25% - if 75% of shares are ragequitted, the proposal will fail automatically as the original circumstances when the proposal was submitted, including access to funds, changes dramatically.
- LunarDAO Squad is based on owning DAO "Shares" - governance power, LunarDAO community is based on the ownership of "Loot".
    - Shares & Loot can be represented by: $VOX = LunarDAO squad shares and $LUNAR = LunarDAO community loot. 

## Terminology

### Governance

* **Community:** People holding loot (or $LUNAR), active in the DAO, non-voting power
* **Squad:** DAO members holding shares, voting power
* **Sentinels:** Eight guardians ([multi-sig](https://lunardao.net/sentinel-committee-announcement.html)) of the DAO treasury
* **Stewards:** [Anonymous](https://lunardao.net/why-anon.html) core-team/founders of the DAO, securing operations (can be exchanged, archived, scaled up)
* **Committees:** Working groups with a specific focus (research, media, education)

### Threshold protocols

**Note:** ***In all cases DAO participants/members are encouraged to setup [anonymized wallets](https://wiki.lunardao.net/anonymizing_assets.html) before joining the DAO!***

The option on restricted governance access/ Squad membership refers to terms *"Social zk-proof"*, *"Squad invites"* and *"Minimal Tribute"* as possible threshold protocols:

**Social zk-proof**

* An anon community member shares a proposal to join the Squad (whether minimal tribute or a short introduction to be presented - yet to be defined).
* Only an existing Squad member can submit a proposal for a new member on chain, which serves as a Squad vouch without sharing further knowledge who knows who.
* The rest of the Squad reads the proposal (and or the initial tribute) and vote on the new member.
* Every new member is encouraged (doesn't have to) to choose a fully anon identity.
* Members can change their forum/chat nicks at will, by which the connection to their wallets are broken.
* This system needs to be worked out well to prevent network mapping (socially and on-chain).


**Squad Invites**

* Every Squad member can add a new Squad member (can be combined with a minimal tribute option).
* The number of invites per Squad member is limited (or limited per time period) -> incentive to chose wisely.
* When adding a new member a short introduction (yet to be defined) including information about initial tribute shall be shared in the Squad.
* Adding a new member is not instant (ie. one week) which allows others to propose to GuildKick the host or a RageQuit themselves, if they disagree with adding the new member. 
* The system is similar to Social zk-proof, without voting and needs to be worked out to prevent the same risks.

**Minimal Tribute**

* A size of a minimal tribute is defined by the Squad.
* Every new member to join the Squad must escrow a minimal tribute to the DAO treasury.
* When a new member joins the DAO Squad, the tribute will be exchanged for equal amount of shares assigned to the new member.

The above mentioned thresholds can be further developed and combined together.

## Questions

Keep in mind that if we were to choose Moloch V3 model, the questions are related for the setup on launch with a possibility to change many of these settings later on. Those changes, or at least a discussion about them can be included in the roadmap, so different options in different phases of the DAO life cycle are already considered.

1. What shall the relation be between the Community and the Squad on Governance (social) level?    

    a) The Squad is (low threshold) permission based or,  
    b) Completely permissionless  

Both have advantages and disadvantages:

*Table 1: Restricted & Permissionless setup; Pros vs Cons*

| | **Restricted** | **DAO** | **Permissionless**| **DAO** |
| --- |--- | --- | --- | --- |
| | **PROs** | **CONs** | **PROs** | **CONs** |
| **Size vs Quality** | Mission aligned Squad | Slower ramp up | No threshold | Ape pump-dump risk |
| **Anonymity** | None | Need a vouching system | More anon friendly | Needs a system to prevent whale manipulation |
| **RageQuit** | Squad members are more involved in the governance | None | Easy re-entry | RageQuit possibly endlessly, can be easier to manipulate |
| **GuildKick** | Any member can propose others to be kicked out | None | None | GuildKick process is a complex process, hard to kick ppl out in this setup |
| **Operation overhead** | Possible to use the Onboarder | More work to onboard ppl manually | Less work with the setup | Hard to GuildKick & keep the DAO aligned with the mission |

2. What shall be the relation between $LUNAR (shares) & $VOX (loot) on economical and technical level.  

    a) Shall $VOX (shares) be non-transferable and $LUNAR (Loot) liquid, or alternatively both liquid or both non-transferable?  
    b) Shall $LUNAR as loot be introduced at launch, later/after launch or not at all?   
    c) Alternatively at launch: shall $LUNAR be sold on the market and $VOX be non-transferable, granting an access to a permissioned squad?  
    d) What would be the ratio, and exchange system between $LUNAR and $VOX be in such setup and what is the best mechanism to prevent $VOX suffer the outcome of $LUNAR market volatility? (ie. If we use a system of burning LUNAR to acquire VOX, how do we calculate the ratio?)  
    e) Alternatively shall $LUNAR be introduced later on as a DAO community token which is not connected to neither shares nor loot of the DAO?

Table 2: Transferable & Non-transferable tokens; Pros vs Cons*

| | **VOX** | **(Governance/Shares)** | **LUNAR**| **(Community/Loot)** |
| --- |--- | --- | --- | --- |
| | **PROs** | **CONs** | **PROs** | **CONs** |
| **Transferable** | Everyone can buy in, possible more organic decentralization | Governance token for investment DAO can suffer under whale speculations, bad distribution, centralization & manipulation | Liquid & accessible, scales up the community | (in case of non-transferable VOX) the relation in between the tokens has to be more sophisticated (ratio, burn mechanism) |
| **Non-Transferable** | The DAO decides on the shares distribution, the token serves the governance, the value = treasury net | higher threshold, wallet address needed | Under the control of the DAO | Limits the access to the community, slows down the launch |

3. Do we want the Squad members to be able to RageQuit even when they voted yes? (In Moloch V2 this was not possible, in V3 it is)
4. What's the best launching model to reach as fair distribution as possible?
5. If LunarDAO is to start with (low threshold) permissioned governance (share based), what has to be done to ensure that people will join on launch?
6. How to keep the core-team operational?


### Points of Consideration

Adding up all the PROs and CONs gives us better understanding of possibilities and consideration for the best design to be chosen for LunarDAO launch.

#### 1. Permissionless vs Restricted

**Fully Permissionless**

The DAO governance is inclusive, the community scales up faster and importantly - it is anon friendlier by default. However, if burning $LUNAR = $VOX (shares) and RageQuit has 0 fees (which we prefer!), people can move in between Community (based on loot) and the governing Squad (based on shares) permissionlessly and without any commitment (vouch threshold entry, minimum tribute, or the undesired locking system). The GuildKick becomes overly complicated (nearly impossible). This challenges some of the main properties of Moloch design and may bring risks to the DAO. It can impact how seriously privacy investors may want to engage. An option would be to look into a combination with non-transferable shares.

**Restricted Governance**

Vouching system means that only Squad members can propose and vote on new Squad member, this brings a challenge to anonymity (read on "social zk-proof" below). On-boarding new members brings more overhead operations. Membership can be restricted by vouch/vote, tribute size, or an invite system (read below in "Squad invite"). The DAO ramp up would be much slower and likely exclude people who don't already have existing connections to the network forming around the DAO in the beginning (unless a system is based on "Tribute minimum" - read below). Restricted governance puts in risk the DAO outreach and growth, however if done well and for a limited period of time (later proposal + vote) such design can defend the DAO Squad from a mission creep and manipulation as it defines the commitment from speculation and allows for a guild kick.


#### 2. Transferable vs Non-Transferable (Loot & Share/ $LUNAR & $VOX)

Based on the mission and community feedback, we believe that the governance token (shares/$VOX) shall NOT be transferable as it represents the governance responsibility and it's value shall represent the shared DAO net value, not a market speculative price. 

**Transferable Loot**

If $LUNAR == Loot (non governing representation of DAO shared value) -> tradable on the market (and burning LUNAR gives VOX/voting power) -> the price of $LUNAR is open to market speculation -> red light for privacy investors. To prevent that the relation between the Loot and Shares must be volatile as well (while a share price is defined: DAO net value / # shares).

**Non-Transferable Loot**

Loot as Shares stays non-transferable, account bound. Loot value = shares value, but Loot does not allow for voting. $LUNAR can be either a symbol representing the non-transferable Loot or serve as a community speculative token, with a possibility to burn and mint equal value of non-transferable loots (or shares in permissionless setup). In such case $LUNAR tokenomics (launch and distribution) must be decided by the DAO Squad. 


## FINAL OPTIONS

Let's summarize the discussion into two possibile models.

### Option 1: Conservative Launch - quality over size

The DAO kick-off is slower, but more sincere, based on mission alignment, commitment and step by step optimization and growth.

- The DAO Squad has a low threshold permissioned membership. Based on *"Social zk-proof"*; a pseudonymous vouching system or a combination of *"Squad Invites"* and *"Minimal Tribute"*. 
- Restricted launch with a plan that after some time/# members a discussion + vote takes place to change using the Onboarder or go fully permissionless.
- The shares/$VOX are distributed to Squad members based on their tribute size. 
- Shares are represented by $VOX and are non-transferable.
- Loot is:
    - a) Represented by $LUNAR and can be acquired by anyone (either at launch as it was planned in the v1 tokenomics or in another way)
        - If $LUNAR in place from launch: Community member accepted as a Squad member burns their $LUNAR into $VOX
    - b) Alternatively the Loot is also non-transferable and represents non-governance shares of RageQuitted Squad members - similar to Moloch v2.
        - In such case Loot != $LUNAR (loot = $VOX which has been ragequitted). $LUNAR launch and function is instead integrated in the roadmap as per #2, e).
- Ragequit based design, with no fee.
- GuildKick included (malicious actors can be proposed to be kicked out of the DAO - force a RageQuit).
- The DAO is built on top of the existing multi-sig safe (for the [reasons explained](https://lunardao.net/sentinel-committee-announcement.html)). A discussion and vote to remove the trusted element will take place after agreed period (ie after 3 months counted from the launch).
- Anyone can submit proposals, only holders of $VOX/shares can vote. 
    - Alternatively only holders of the loot or shares ($LUNAR or $VOX) can submit a proposal.
- The DAO is launched on existing [contracts](https://github.com/Moloch-Mystics/Baal) and [UI by DAOhaus](https://summon.daohaus.fun/). 
- Further upgrades and customization will be discussed in the community and voted upon.
- A management/admin fee of 0.5% is calculated and sent to core-team multi-sig wallet once every 3 months (ETH: 0xAb501a8Eb58c9780eb04D683feB504fcE391A2DD)
- For extra costs/expenses such as dev, research, education etc a LIP is submitted and voted upon.

### Option 2: Inclusive Launch & Anon maxi (at any cost)

The DAO token and governance power is accessible to anyone, allows for faster community scale up. Such setup allows for governance token speculation which can suffer both in terms of price as well as the poor quality of governance decisions and possible manipulation.

- Permissionless, no threshold to become a member.  
- Anyone can get $LUNAR (loot).  
- To get $VOX (shares), burn $LUNAR.  
    - or option b): To get $VOX stake $LUNAR into the treasury.
- Possible: Early exit penalty: the member exits with a slightly smaller amount than at entry (done by a time escrow of decided % of their tribute which unlocks after agreed time period) - non desirable as it's a risk for privacy investors.
    - or option b): No fee for exiting, assumption that it is unlikely that RageQuit will be generally misused. Change this through proposal if misuse occur.  
- People can RageQuit and rejoin for eternity.
- No GuildKick is applicable in permissionless setup as the assets can be moved around easily. To circumvent that requires freezing minting and preventing token to be transferred and only then proposing a GuildKick.  
- Anyone can submit proposals, only holders of $VOX can vote.
- The DAO is launched on existing [contracts](https://github.com/Moloch-Mystics/Baal) and [UI by DAOhaus](https://summon.daohaus.fun/). 
- Further upgrades and customization will be discussed in the community and voted upon.
- A management/admin fee of 0.5% is calculated and sent to core-team multi-sig wallet once every 3 months (ETH: 0xAb501a8Eb58c9780eb04D683feB504fcE391A2DD)
- For extra costs/expenses such as dev, research, education etc a LIP is submitted and voted upon.


## Conclusion

LunarDAO is an anonymity-first organization. However our mission is bigger than that. From the option 1 and option 2 (and anything between and beyond) the largest contradictions to resolve are in remaining as anon as it is possible (on ETH) while staying true to the aims of the DAO. Looking into investment DAOs based on Moloch V1 & V2, listening to the allies in chats and multiple meetings with builders, we believe that LunarDAO should not kick-off as an experiment, instead start on well tested mechanisms. 

However Moloch V3 seems to be the best fitting design because of its optionality - which allows for a 100% permissionless DAO - the implementation of such logic for a mission aligned investment DAO was not tested. If LunarDAO were the first one to experiment with the new models, it shall be done on a strong foundation, based on a proper community discussion and preferably Squad vote, which is impossible to have before the DAO itself is well established. 

If we were to choose option 1, the threshold needs to be minimal, non-doxxing and the protocol must be thought through to protect the members. We have already recommended in our [docs](https://wiki.lunardao.net/anonymizing_assets.html) to use Aztec or TornadoCash mixers, ensure network protection and [change RPC](https://wiki.lunardao.net/change_rpc.html) as a basis to join LunarDAO.

If we were to base the launch on option 2, the protection against governance speculation and manipulation must be put in place and the (dis-)ability of an easy GuildKick well evaluated.

## To be or not to be...

However there are many important details to decide upon, giving all the pros and cons, the main discussion is in between the presented options or their timing:

### A) Shall LunarDAO launch on a variation of OPTION 1 and eventually change towards OPTION 2 based on future voting (as a phase 2)?

or:

### B) Shall LunarDAO launch straight on a variation of OPTION 2?  

As decided in LunarDAO [Objectives & Key Results for February](https://github.com/lunardao/okr/blob/master/okrs_february_23.md) the DAO structure shall be finished and approved by the community by March 6th. To leave time for the final tweaks and the deployment, we would like to have the DAO structure agreed upon by February 26th.

**LET'S DECIDE THE BEST WAY TOGETHER, JOIN THE [DISCUSSION](https://forum.lunardao.net/t/tokenomics-lunar-vox/89/45)!**

**[SUPPORT THE DEVELOPMENT](https://github.com/lunardao/dao/blob/main/SUPPORT.md) OF LUNARDAO ARCHITECTURE!**
