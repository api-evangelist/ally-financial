# Ally Financial GraphQL Schema

Ally Financial is an online bank and auto finance company offering a broad range of financial products including checking and savings accounts, money market accounts, CDs, IRAs, investment and brokerage accounts, auto loans, personal loans, mortgages, home equity products, credit cards, and dealer financing services.

## Overview

This conceptual GraphQL schema models the core domains of Ally Financial's platform:

- **Banking** — deposit accounts, balances, transaction history, payments, transfers, and cards
- **Lending** — auto loans, personal loans, mortgages, and home equity lines
- **Investing** — brokerage accounts, IRAs, and investment holdings
- **Auto Finance** — dealer floor plans, remarketing, portfolio management, and manufacturer programs
- **Identity and Access** — customer profiles, addresses, contacts, API keys, and tokens

## Schema Source

This is a conceptual schema derived from Ally Financial's publicly documented REST API capabilities at [https://developer.ally.com/](https://developer.ally.com/) and supplemented by analysis of their product offerings across banking, investing, and auto finance verticals.

## Types Summary

| Domain | Types |
|---|---|
| Deposit Accounts | BankAccount, CheckingAccount, SavingsAccount, MoneyMarketAccount, CertificateOfDeposit, IRAAccount |
| Investment Accounts | InvestmentAccount, BrokerageAccount, Holding, Position |
| Lending | AutoLoan, PersonalLoan, Mortgage, HomeEquityLoan, HomeEquityLineOfCredit |
| Balances | AccountBalance, AvailableBalance, LedgerBalance |
| Transactions | TransactionHistory, Transaction, Merchant |
| Payments and Transfers | Payment, Transfer, ACHTransfer, WireTransfer, ZelleTransfer, DirectDeposit |
| Protection | OverdraftProtection, OverdraftTransfer |
| Cards and ATMs | Card, DebitCard, CreditCard, ATMLocation, Branch |
| Rates | Rate, HistoricalRate, APY, APR |
| Quotes | Quote, AutoFinanceQuote |
| Auto Finance | AutoFinance, CarDealership, DealerSalesProgram, FloorPlanCredit, Remarketing, CustomerPortfolio |
| Manufacturer Programs | FordCredit, GMFinancial, ChryslerCapital |
| Fees and Records | SalesTax, PaymentRecord, AutoPayment |
| Customers and Identity | BankCustomer, BusinessCustomer, Profile, Address, Contact, Partner |
| API Platform | APIKey, Token, Webhook, OAuthClient |
| Documents | Statement, TaxDocument |

## Usage

This schema is intended as a reference for:

- API design discussions and GraphQL gateway modeling over Ally Financial REST endpoints
- Developer tooling and client SDK generation
- Integration planning for fintech, auto dealer, and enterprise customers
- API catalog enrichment and discoverability

## Schema File

See `ally-financial-schema.graphql` for the full type definitions.
