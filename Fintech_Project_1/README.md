# Medipass: An Australian Healthcare Digital Payment Solutions Company

## Overview and Origin

* **Name of company**<br>
  Medipass Solutions Pty Ltd 2021, ABN (21 615 345 536)

* **When was the company incorporated?**<br>
  14th October 2016

* **Who are the founders of the company?**<br>
Founder: Pete Williams (Co-Founder and CTO), Adrian Perillo (Co-Founder and COO).

* **How did the idea for the company (or project) come about?**<br>
In December 2014, Pete Williams co-founder of Localz Pty Ltd won the National Australia Bank’s “NAB Labs’ inaugural Hackathon” with the formative work of Medipass Solutions. This work, which allowed health providers to accept payments without the need for an EFTPOS terminal, impressed Jonathan Davey who was the Executive General Manager for NAB Labs & NAB Ventures at the time. Davey could see the potential improvements Medipass could make to their already long established Health Insurance Claiming At Point of Sale (HICAPS) platform. HICAPS Pty Ltd is a wholly owned subsidiary of National Australia Bank Limited (ABN 12 004 044 937 AFSL and Australian Credit Licence 230686) and has been the leading provider of Point of Sale Health Insurance claiming, Medicare claiming and EFTPOS terminals in the Australian Health Care sector since June 1998. 

    Pete and Jonathan recruited the help of Adrian Perillo (Head of Consumer Product for Medibank Private Insurance Company from Mar 2014 to Dec 2015) to work with them to bring HICAPS up to speed with other mobile payment platforms like Uber, etc.. by incorporating co-payments from Private Health Insurance (PHI) Companies and Government backed funding such as Medicare, Department of Veterans Affairs into health care practitioners’ practice management systems. They also saw potential to use Medipass for other data driven, patient decision making applications like practitioner shopping, health care quoting and online appointment booking platforms. 

* **How is the company funded? How much funding have they received?**<br>
    Seed Funding for Medipass Solutions was announced 17th Feb, 2017 by NAB Ventures Equity Investment, however the funding amount was undisclosed. As a guide though, 3 of the 5 seed funding rounds by NAB Ventures from 2017 to 2020 ranged from A$2,500,000 to A$7,000,000. Therefore, it could be reasonably assumed that Medipass received funding equal to an amount somewhere in this range. At this time there was also a multiyear Commercial Agreement between NAB Ventures and the Medipass Solutions team to work within the HICAPS mobile platform for an undisclosed sum. They sought a Series A funding round in October, 2020.  

    On May 10, 2021 Medipass Solutions was acquired by Tyro Payments for A$22,500,000. 


## Business Activities:

* **What specific financial problem is the company or project trying to solve?**<br>
    The purpose Medipass Solutions was born to address is most succinctly explained by it’s slogan: “Digital payment solutions to help healthcare providers get paid fast”. More specifically Medipass sought to optimise what they believed to be the 3 key areas of the healthcare transaction for:<br>
    >**1. Patients:** A simplified and transparent experience including ease of locating, booking and managing a health practitioner appointment, estimating out-of-pocket costs for a consultation ahead of time and on the spot claiming.<br>**2. Private & Public Health funds/payers:** Reduced claim processing overheads, simple pay and claim functionality and improved fraud controls.<br>**3. Health practitioners:** Electronic booking, claiming and payments, reducing administrative needs and simplifying the payment process. 

* **Who is the company's intended customer?  Is there any information about the market size of this set of customers?<br>
What solution does this company offer that their competitors do not or cannot offer? (What is the unfair advantage they utilize?)**<br>
    Medipass Solutions’ intended customers are healthcare professionals. More specifically, Medipass then integrates their payment platform into the clinical software the healthcare professionals use to manage their patients. Thus making the entire healthcare transaction as efficient as possible through mediums the healthcare professionals are already familiar with (ie. their clinical software and HICAPS). 

    According to IBIS World, in January 2021 there were 156,406 registered Healthcare Service Businesses in Australia. This total is almost entirely comprised of General Medical Practices and Allied Health Businesses who would utilise the types of services Medipass offers.   
    Patient wise, the Australian Prudential Regulation Authority (APRA) reported the number of people covered by Private Health Insurance for the financial year 2021 was 11.34 million people with Private Health Insurance Membership revenue for the 2021 financial year totalling  A$25.7b. 

    While Medipass formally entered the retail healthcare market in 2017, a company called Tyro Payments Limited (ACN 103 575 042 AFSL 471951) had long been touting their EFTPOS and PHI payment services to Private Healthcare Practices. Back in 2003, Entrepreneurs Paul Wood, Peter Haig and Andrew Rothwell founded Tyro in response to the RBA’s call for greater competition within the EFTPOS space, particularly to challenge the big 4 banks. In 2005, Tyro was the first tech company in Australia to acquire a bank licence and they were the first to offer cloud based EFTPOS solutions in 2007. Tyro was also the first to launch integrated EFTPOS Medicare claiming in 2009 and integrated PHI claiming into their EFTPOS terminals in 2014, 3 years before Medipass hit the market. However, the problem Tyro faced was that HICAPS was first to market (1998) and by 2014 already had 36 Private Health Funds (99% of the PHI market at that time) incorporated into its payment system. Added to that issue was that Tyro was still in its infancy as a “bank” and could not compete with NAB from a financial perspective. To grow their business quickly enough to compete, Tyro had to offer its payment solutions across the broader retail market which detracted from its Healthcare focus and ultimately kept it behind the already building mass adoption HICAPS had established. 

    In the end, Tyro (ASX:TYR) couldn’t compete and acquired Medipass for A$22.5m on the 10th May 2021. Jonathan Davey had also resigned from NAB in Dec 2019 to become CEO of Medipass in May 2020 and it could be speculated that he cut the ties between NAB, HICAPS and Medipass upon resignation. 

    Some other very weak competitors in this space, include: Payveris - https://www.payveris.com/company/ -  and Dejamobile - https://dejamobile.com/about/ . however both companies have diverse target markets and neither specifically focus on healthcare. 

* **Which technologies are they currently using, and how are they implementing them? (This may take a little bit of sleuthing–– you may want to search the company’s engineering blog or use sites like Stackshare to find this information.)**<br>
    The technologies behind Medipass Solutions are best explained from the two sides of the platform, the front end and the back end. 

    At the backend, Medipass connects to Funders such as Private Health Insurers (PHIs), Medicare, Department of Veterans Affairs (DVA), iCare, Workcover and NDIS. Each integration partner sends a payload which is a submission in JSON format using objects within the payload including FUNDER objects (pt name, DOB, PHI #) , TREATMENT objects and PRACTITIONER objects. Once submitted, Medipass uses Webhooks custom callbacks to approve or deny the claim on the platform.  

    At the front end, Medipass is hosted on Amazon Web Services (AWS)  and connects to the Healthcare Practitioner’s Practice Management Software via relevant programming languages, most commonly React and Ruby on Rails. The console is updated via Restful APIs. A software development kit using Java Script iFrame is the container used for the payment system and works much like the Paypal pop-up console does when purchasing on eCommerce sites. 

    The Medipass payment process follows these four steps:<br>
    >**1. Validation of the patient:** Workercover ID / claim number, PHI number, Medicare number, DVA number, iCare number, NDIS participant number.<br> 
        **2. Submission of the claim for treatment:** Treatment Item number and date of service.<br> 
        **3. Adjudication to ensure due diligence:** Cross referencing, duplicate checking, ensuring claim falls within the insurers’ guidelines.<br>
        **4. Settlement:** Linking to insurers bank, like bank feeds on institutional level, pulling and putting the data through APIs, Workcover claiming. 

    For the sake of this assignment this section has been kept brief however a comprehensive table of technologies utilised by the Medipass platform can be found here (Source: https://builtwith.com/detailed/medipass.com.au ). 


## Landscape:

* **What domain of the financial industry is the company in?**<br>
    Medipass crosses a few domains within the financial industry, namely payment systems, retail banking and insurance. 


* **What have been the major trends and innovations of this domain over the last 5-10 years?**<br>
    Since 2011 Payment Systems have seen movements away from cash, cheques and even plastic towards online payments, particularly in the last 18 months due to COVID-19. Companies like Amazon, Google and Paypal have steered this ship rapidly over this time. Smartphone development has also been a major catalyst for contactless and online payments and now Cryptocurrencies are proving they are here to stay and are now officially “currency” in a growing number of countries. Needless to say, payment regulations have struggled to keep up with the pace. Australia follows similar patterns to North America in this domain and Electronic Transfer payment values increased 8.9% to USD$55.8 trillion in 2019, while the volume of B2B electronic payments were up by 12% at 4 billion items in 2019. 

## Results

* **What has been the business impact of this company so far?**<br>
There has been rapid adoption of Medipass since it’s inception. The growth in number of providers registered and growth in the number of transactions over 2019 FY was over 20% month on month. During COVID there was even more rapid adoption of users due to the significant rise in Telehealth consultations given that Medipass offers non-EFTPOS terminal solutions and claims and payments can be made on the Medipass Solution via Desktop, iPads, iPhones, etc… All of this has proven to produce better healthcare outcomes due to the reduction of barriers to access the healthcare.  

* **What are some of the core metrics that companies in this domain use to measure success? How is your company performing, based on these metrics?**<br>
In the Payment Processing sector it is generally agreed that there are 3 key payment conversion KPIs:<br>
  >**1. Payment Conversion Rate:** This metric indicates how many transactions on the whole were declined (eg. if 20 out of 40 transactions were successful the you have a 50% conversion rate). Through the simple iFrame console, Medipass offers many front end conveniences to patients and practitioners to ensure their payment processes are clear and simple to perform.<br>
**2. Conversion rate by Bank:** Different banks have different rates of declined transactions due to various factors including changing regulations and mismanaged payment processing. Medipass outperforms all competitors in this domain as it was backed by and built for NAB, Australia’s 4th largest bank. <br>
**3. Conversion Rate by Payment Method and Card Type:** Payment method offerings affect this metric significantly. Medipass offers every payment method under the sun and allows Funders to be appropriately informed of all relevant details of the claim and claimant.<br>
Medipass has notched a 380 per cent jump in new user sign-ups over the past month, with 13,000 providers now linked to the terminal-free payments platform that lets users settle medical bills without tapping a card. The majority of that growth has come from telehealth services.

* **How is your company performing relative to competitors in the same domain?**<br>
As explained above. Medipass has led all competitors in its specific domain of healthcare payment processing as explained above, it has the lion’s share of all metrics. It should be noted that Medipass was nominated for a Finnie award in (Emerging FinTech Organisation of the Year) in 2018 further supporting its competitiveness across the entire FinTech industry. 

## Recommendations

* **If you were to advise the company, what products or services would you suggest they offer? (This could be something that a competitor offers, or use your imagination!)**<br>
    Although Medipass are leaders in their domain, I believe that there are further opportunities to develop the platform by developing their own patient-centric electronic medical records (EMRs) system. Most of these systems are easily build now on SaaS platforms which would be a no brainer for Medipass. If they wanted to compete for the future, I believe this EMRs system could be built on blockchain technology utilising a distributed ledger. 

    Furthermore they could use Smart Contracts for Private Health Insurance. Various healthcare domains such as medical devices, pharmaceuticals, wholesalers, insurers and healthcare professionals, can authenticate their identities as organisations, log contract details, and track the transactions of goods and services, and payment settlement details for those goods and services. 

    By having shared digital contracts between manufacturers, distributors and healthcare organisations logged on a blockchain ledger, rather than each player having their own version of contracts, they can significantly reduce disputes over payment chargeback claims for prescription medicines and other goods because Insurers are notorious for changing their pricing structures. In America, there are over one million chargeback claims made between these players every year, more than 5% of which are disputed, requiring lengthy manual resolution.


* **Why do you think that offering this product or service would benefit the company?**<br>
    As explained above, utilising blockchain and open ledgers would enhance the security and control of all Healthcare transactions and greatly reduce administrative costs related to chargebacks and failed claims, etc... 

* **What technologies would this additional product or service utilize?**<br>
    Blockchain. 

* **Why are these technologies appropriate for your solution?**<br>
    These methods of supply chain management enable supply partners and funders in the healthcare sector to become fully digitised and could offer automated contractual processing. 

    Similarly, shared smart contracts can be used to manage medical insurance contracts for patients, where up to 10% of claims are disputed. Like in other use cases, once this data is digitised and easily accessible, insurance providers can use more advanced analytics to optimise health outcomes and costs.



## References

- Medipass website: For Company details - https://medipass.com.au/ 

- Australian Business Register: For Medipass Company details - https://abr.business.gov.au/ABN/View/21615345536 

- Australian Securities and Investments Commission: For Company details - https://connectonline.asic.gov.au/RegistrySearch/faces/landing/panelSearch.jspx?searchText=615345536&searchType=OrgAndBusNm&_adf.ctrl-state=figkzje6w_15 

- Linkedin: To find out more about key personnel<br> Peter Williams (Founder) - https://www.linkedin.com/in/williape/<br>Adrian Perillo (COO) - https://www.linkedin.com/in/adrianperillo/<br>Jonathan Davey (COO) - https://www.linkedin.com/in/jonathan-davey/?originalSubdomain=au 

- NAB News 17.02.2017 - NAB RE-IMAGINES THE HEALTHCARE CUSTOMER EXPERIENCE - 
https://news.nab.com.au/nab-re-imagines-the-healthcare-customer-experience/ 

- The Sydney Morning Herald 13.04.2020 - Startups spruik privacy smarts in race for telehealth bonanza by Emma Koehn : For news and editorial content for more background on the company from inception - https://www.smh.com.au/business/small-business/startups-spruik-privacy-smarts-in-race-for-telehealth-bonanza-20200409-p54ild.html?fbclid=IwAR3K5KD1Zk3L7PlbewQKM8e2SYEdP1-fW9kV9L7j7hxGsYryICeK8AvSKi8 

- NAB News - Interview Jon Davey & Pete William -
https://nabnews.efront-flare.com.au/wp-content/uploads/2017/02/170216-Interview-Jon-Davey-Pete-William-NAB-News.mp3 

- Localz website - for company details - https://www.localz.com/about-us/ 

- Australian Business Register: For Localz Company details - https://abr.business.gov.au/ABN/View?abn=49166395062 

- Fintech Chatter Podcast: ep “Fintech Organisation of the Year - Medipass” 07.10.2020- https://podcasts.google.com/u/1/feed/aHR0cHM6Ly9mZWVkcy5idXp6c3Byb3V0LmNvbS83MDMyNDkucnNz/episode/QnV6enNwcm91dC01NzQxNjgw?sa=X&ved=0CAIQuIEEahcKEwigtMPXjsvxAhUAAAAAHQAAAAAQAg 

- HICAPS website: For Company Details - https://www.hicaps.com.au/common/about 

- Crunchbase Seed Funding Rounds - Filtered for NAB Ventures with 5 results including Medipass (undisclosed) -  https://www.crunchbase.com/discover/funding_rounds/12cb2f7bd8f3f03053fec705880752d6 

- Crunchbase Aquisitions - Filtered for Medipass with 1 result, Tyro Payments for A$22.5m - 
https://www.crunchbase.com/acquisition/tyro-payments-acquires-medipass-solutions--679e859e 

- IBIS World - Healthcare Service Data 2021 - https://www.ibisworld.com/au/bed/private-health-insurance-membership/2153/ 

- NCBI - X - https://www.ncbi.nlm.nih.gov/pmc/articles/PMC5900819/ 

- Tyro website: For company details - https://www.tyro.com/about-tyro/ 

- Australian Business Register: For Tyro Company details  - https://abr.business.gov.au/ABN/View?abn=49103575042 

- What is a Seed, Series A, B, C Funding Round? By Anthony Lieu, 15.09.2020 - https://legalvision.com.au/what-is-a-seed-series-a-b-c-funding-round/ 

- Nookal Practice Management Software - Setting up Medipass Integration - https://www.nookal.com/help/setting-up-medipass 

- Builtwith website - For publicly available, detailed list of technologies used for platform - https://builtwith.com/detailed/medipass.com.au 

- Phone interview with Fahad Rahman-Safe (Medipass - Head of Partnerships) 10.45-11.30am 09.07.2021 - discussion and explanation of technologies used by Medipass at back and front ends of the platform. IP was not exposed during the conversation, nor was there a NDA. 

- Australian Financial Industry Sectors - Austrade website  - https://www.austrade.gov.au/international/buy/australian-industry-capabilities/financial-services 

- NAB Annual Financial Report 2017 - https://www.asx.com.au/asxpdf/20171114/pdf/43p69wv97sw91v.pdf 

- NAB Annual Financial Report 2018 - https://www.nab.com.au/content/dam/nabrwd/documents/reports/corporate/2018-annual-review-accessible-version.docx 

- Payment Processing Metrics - https://home.bluesnap.com/snap-center/blog/payment-metrics/ 

- Blockchain Healthcare Use Cases - https://openledger.info/insights/blockchain-healthcare-use-cases/ 

- 5 blockchain healthcare use cases in digital health - https://stlpartners.com/digital-health-telecoms/5-blockchain-healthcare-use-cases/ 
