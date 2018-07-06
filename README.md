# European Investment Bank Blockchain Challenge

The European Investment Bank (EIB) Finance team invited its 25 major counterparties in the banking sector to an annual forum to reflect on common issues, such as financial instruments processing, regulation, infrastructure, and organisational management.
For 48 hours, the European Investment Bank headquarters became home to a “codefest”. 56 coders from all over the world worked, ate and slept in the same building with the goal of improving financial transactions using blockchain technology. The EIB called the event “The Blockchain Challenge”.
# The Challenge
At the EIB Blockchain Challenge, the first competition of its kind organised at the EU bank, a group of 56 highly motivated coders were invited to use blockchain and process automation technologies to revolutionise the way financial transactions are processed.
These coders competed for two days (and two nights!) to come up with blockchain solutions to a given financial instrument.

 # Definition
 ## 1.1 What is a Commercial Paper (CP)?
Commercial Paper is an unsecured, short-term debt instrument issued by a corporation, typically for the financing of accounts receivable, inventories and meeting short-term liabilities. A Commercial Paper is usually issued at a discount from face value and reflects prevailing market interest rates.
 
 ## 1.2 Why EIB issues Commercial Papers?
Euro Commercial Paper (ECP) is an unsecured general obligation in the form of a promissory bearer note, issued on a discount or interest-bearing basis by large commercial and industrial organizations. Because ECP can offer unsecured short-term funding that is often cheaper than borrowing from a bank, it is an attractive source of such funding.The EIB borrows the short-term funds necessary for the performance of its tasks in the international money markets mainly under its Global Commercial Paper Program. This program allows issuance of EIB commercial papers in New Global Note form and commercial papers eligible for ECB collateral operations.

- **Access to cheaper funding**
Commercial Papers are used not only to diversify the way the bank finances itself, but also as an inexpensive way to raise funds. This form of unsecured short-term funding is often cheaper than bank loans or overdraft credit lines and can therefore be used to finance a number of different purposes, including short-term working capital.

- **Dealing and investing in Commercial Papers**
After the appointment of the banks and the signing of the documentation, the issuer can use the programme to draw down funds. The issuer will notify the dealers about the amount of funding required and for which period the funds will be required. The dealers will advise the issuer of the current investor appetite and the approximate price levels. Then, the issuer will allocate a share of the required amount to each dealer so they can sell it to investors.

- **Choose the Issuing and Paying Agent (IPA)**
Before the program can begin, the issuer needs to appoint an IPA. The IPA collects details of the trades from the issuer and the dealer, and then obtains the International Securities Identification Number (ISIN) codes before arranging payment. ISIN codes are allocated to each trade in the ECP market. Each ISIN can be unique to a particular trade and assists with identification during clearing and settlement, while transactions happening on same value date can be associated with the same ISIN code.

## 2. How does the flow work?
The following is an explanation of the flowcharts provided on pages 4 to 9. The first flowchart is a simple representation of the flow (General Simple Flowchart). The following (General Flow) is a more detailed explanation, describing the critical phases of the European Commercial Papers trade process (Configuration and Settlement phases).
In order to simplify the representation and to clearly understand the flow, the overall process has been divided in 4 parts: Pricing Phase, Trading Phase, Configuration Phase, and Settlement Phase. Each phase has its own flowchart describing the actions required to fulfill the tasks. These charts, taken together, represent the entire flow from beginning to end.
Here, are the explanations for each different phase:

## 2.1 Pricing
The Commercial Paper flow starts from the Front Office Liquidity Management, which is in charge of managing the short-term investments and providing the funds required for operations. From Back Office Treasury (BOT) a liquidity plan is sent to the Front Office, which, according to this report, decides how much to issue.

## 2.2 Trading
Commercial Paper rates are published in Bloomberg or sent via mail (generally the major global currencies, while other currencies rates are delivered upon request), with their respective levels. Front Office Liquidity Management starts receiving deal requests from counterparts via Bloomberg chat. At this stage, much like any common trade, agreement on price, amount and date is made and the Bloomberg confirmation message VCON defines the terms of the trade. Here is an example of the rates table:
|   | EUR | USD | GBP |
| ------ | ------ | ------ | ------ |
| **1M** | 1.00 | 1.00 | 1.00 |
| **2M** | 1.00 | 1.00 | 1.00 |
| **3M** | 1.00 | 1.00 | 1.00 |
| **4M** | 1.00 | 1.00 | 1.00 |
| **5M** | 1.00 | 1.00 | 1.00 |
| **6M** | 1.00 | 1.00 | 1.00 |
| **9M** | 1.00 | 1.00 | 1.00 |
| **1Y** | 1.00 | 1.00 | 1.00 |
*1.00 used as exapmle

At this point, Front Office asks Middle Office for configuration in order to book the instrument and commit the transaction.

## 2.3 Configuration
With confirmation of the trade obtained, Front Office has to indicate if the counterparty is a **dealer** or a **non-dealer**.
A counterparty is defined as a dealer when it can sell its own CP by providing the ISIN code for it.
Only the dealer can and must provide the ISIN code, since this is one of its duties in the process.
In case the counterparty is a dealer, Front Office LM forwards directly a request for instrument configuration to the dedicated team (Middle Offfice - SPBS/System and Data Management).
If, by contrast, the counterparty is a non-dealer, Front Office LM forwards a request to Back Office Treasury to obtain an ISIN code. In both cases, the instrument configuration is made in parallel with the ISIN request and check.
**How BOT obtains the ISIN code?**
Back Office Treasury refers to EPIM (European Pre-Issuance Messaging) service to provide an ISIN code for ECP trades where EIB acts as a dealer. The EPIM service to EIB is provided by Citibank, through its platform: CitiDirect for Securities. BOT fills the request with all the CP details provided by Front Office LM and, via CitiDirect (who forwards the request to the ICSD - the custodian), receives an ISIN code. At this stage, Back Office Treasury informs Front Office and the Counterparty.

## 2.4 Settlement
Once the instrument is configured, settlement can take place. BOT is the division responsible for settlement operations, where checks and validations of instrument details are made. After a four-eyes check, involving value date, trade date, nominal amount, etc., a SWIFT message (MT599) is sent to Citibank to commit the transaction (as Citibank is the third party provider/IPA for this type of operation) and another MT599 is sent to the counterparty as trade confirmation. The ICSD (International Central Security Deposit), which is a depositary agent, receives the Commercial Paper from the IPA and the money from the counterparty. It then allocates the money in the ElB's IPA account and the Commercial Paper in the counterparty's account.
Once the IPA (Citibank) receives the amount, it credits the funds in the relative EIB account with the IPA.
At which point, the settlement is executed and the process is concluded.

## 3. Term sheet example
### EXAMPLE FORM OF LISTING TERM SHEET
BANK XXXXXXXXXXXXXXXX
$ 30,000,000,000 U.S.-Commercial Paper Program (the "Program")
guaranteed by
BANK XXXXXXXXXXXXXXXX
Issue of $ 250,000,000 due 08 September 2011 Discount Note

The particulars to be specified in relation to the issue of the Notes are as follows:
1. **Issuer:** BANK XXXXXXXXXXXXXXXX Guarantor: BANK YYYYYYYYYYY
2. **Type of Note:** Commercial Paper
3. **Dealer:** BANK XXXXX & Co.
4. **Aggregate Principal Amount:** $ 250,000,000
5. **Issue Date:** 08/06/2018
6. **Maturity Date:** 08/12/2018
7. **Discount rate:** 0.85%
8. **Delivery:** Against Payment

PROVISIONS RELATING TO INTEREST (IF ANY) PAYABLE
12. **Fixed Rate Note Provisions:** Not Applicable
13. **Floating Rate Note Provisions:** Not Applicable

GENERAL PROVISIONS APPLICABLE TO THE NOTES

14. **Listing and admission to trading:** XXXX Stock Exchange
15. **Ratings:**
The Notes to be issued under the Program have been rated:
Standard & Poor’s: X+
Fitch Ratings: X- 
Moody's: AX-

16. **Clearing System:** ClearingHouseXY
17. **Issuing and Paying Agent:** BankY
18. **Listing Agent:** BankJ
19. **Common Code/ISIN:** Not Applicable.

LISTING AND ADMISSION TO TRADING APPLICATION
This document constitutes the Listing Term Sheet in relation to the Notes, including summarizing the Final Terms required to list and have admitted to trading the issue of the Notes described herein, pursuant to the BANK XXXXXXXXXXXXXXXX

## 5. Glossary for Commercial Papers
**CCB: Cash Correspondent Bank** - financial institution that acts as an agent on behalf of other financial institutions, usually foreign banks, providing services such as intermediation where two banks have no established agreement.
**CitiDirect for securities:** Platform offered by Citibank through which the EIB can make ISIN requests.
Commercial Paper:  an unsecured, short-term debt instrument issued by a corporation, typically for the financing of accounts receivable, inventories and meeting short-term liabilities.
**Dealer:** A counterparty is defined as a dealer when it can provide by itself an ISIN code. More importantly, a dealer can trade on behalf of the party it assists.
**DVP: Delivery Versus Payment** - Delivery versus payment (DVP) is a securities industry settlement procedure in which the buyer's payment for securities is due at the time of delivery.
**EPIM: European Pre-Issuance Messaging** - is a robust ISIN request and allocation system that automates and improves the process of issuing CPs.
**European Commercial Paper:** A European commercial paper (ECP) is an unsecured, short-term loan issued by a bank or corporation in the international money market, denominated in a currency that differs from the domestic currency of the market where the paper is issued.
**IPA: Issuing and Paying Agent**  A paying agent is an agent who accepts payments from the issuer of a security and then distributes the payments to the holders of the security. Also known as a "disbursing agent."
**ISIN code: International Securities Identification Number** - The ISIN code is a 12-character alphanumeric code that serves for uniform identification of a security through normalization of the assigned National Number, where one exists, at trading and settlement.
**ICSD: International Central Securities Depository** - is a specialised financial organization holding securities {ex: commercial papers) so that ownership can be easily transferred through a book entry rather than the transfer of physical certificates. This allows brokers and financial companies to hold their securities at one location where they can be available for clearing and settlement.
**SWIFT: Society for Worldwide Interbank Financial Telecommunications** - SWIFT uses a standardized proprietary communications platform to facilitate the transmission of information about financial transactions. Financial institutions securely exchange this information, including payment instructions, among themselves.
**SWIFT Message:** Message types are the format or schema used to send messages to financial institutions on the SWIFT network.
**SWIFT MT(Message Type)202:** Message to order the movement of funds to the beneficiary institutions (bank to bank cash transfer).
**SWIFT MT210:** Message to notify the receiver that it will receive funds in a determined account (details included).
**SWIFT MT599:** free format message used to send details about a security transaction.
**SWIFT MT543:** Message to instruct delivery of financial instruments (ICSD), against payment (DVP), to a specified counterparty.
**SWIFT MT541:** Message to instruct a receipt of financial instruments (ICSD), against payment (DVP), to a specified counterparty.

## 5.1 Internal EIB Glossary
**FI:** Finance Directorate
**FI/TRE:** Treasury department of the Finance Directorate
**Fl/PRO:** Planning and Settlement Department of the Finance Directorate
**FI/SPBS:** Strategy, Policies & Business Support Department of the Finance Directorate
**FI/TRE/LM:** Liquidity Management Division of the TRE department. Defined as “Front Office”, it is in charge of dealing with the counterparty in the money market and trading financial instruments.
**FI/PRO/BOT:** Back Office Treasury of the PRO Department. Defined as “Back Office”, it is in charge of dealing with the execution of settlement and the validation of the transactions.
**FI/SPBS/SDM:** Systems & Data Management division of the SPBS Department. Defined as “Middle Office”, it is in charge of dealing with configuration of the instrument in the WSS (Finance Kit) internal system.
**WSS/FK:** Wall Street Suite - Finance Kit is the IT system used to manage Front and Back Office Treasury and Borrowings operations.
**Bloomberg Terminal:** Bloomberg terminal is a computer system offering access to Bloomberg's data service, news feeds, messaging and trade execution services.
**VCON BB Ticket:** Confirmation that takes place in Bloomberg once the parties agree with the terms of the deal.
