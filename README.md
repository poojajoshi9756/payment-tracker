# payment-tracker
Some assembly required.

This application is a simple spending tracker/budgeting service that can be used to monitor your finances across any payment mechanism (credit card, debit card, cash sharing app), that has purchase notifications via email. Please see the associated blog post for the inspiration behind the application.

The basic flow for the application is as follows: purchase notifications via email are auto forwarded to a Zapier service. Zapier sends the email subject and body via a HTTP POST request to the Python Flask API endpoint. The API parses the transaction information (description/amount) from the email body, assigns it a category, and writes the transaction to a Google Sheets workbook. All expenses across any payment mechanism can be viewed on the Sheets workbook, along with monthly summaries.

These instructions will walk you through how to set up the application for yourself and host it on Heroku. Fork and clone this repo to get started.
