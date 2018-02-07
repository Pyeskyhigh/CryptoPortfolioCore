# Digital Asset Central Portfolio
A digital asset personal portfolio using CCXT

DACP is a library that pools together the ledger history and balance sheets of all the exchanges an
investor uses. The library will allow for the access of the dataset and commands that can be used
with it. The library uses CCXT (CryptoCurrency eXchange Trading Library) in order to pull the
information from exchanges.

[CCXT](https://github.com/ccxt/ccxt) serves as a library for the access to all the API's for Cryptoasset Exchanges. By using this as a tool, DACP will work by using this library as a way to access all exchanges and build a
dataset with all the personal information of a user.

## License

This repository is licensed under the MIT License. Details can found in the [license file](https://github.com/Pyeskyhigh/DACP/blob/master/LICENSE).

## Contributors & Followers

Help is greatly appreciated as long as people follow the [Contributing]() rules and the [Code of
Conduct](https://github.com/Pyeskyhigh/DACP/blob/master/CODE_OF_CONDUCT.md).


## Layout of API

The following is a preliminary design of the layout of the library.

![picture](./misc/Layout_of_API.png)

**Command Details:**

* Add Exchange: <br />
   Params = Exchange name, API key, OTHER INFO TO ACCESS ACCOUNT. <br />
   Return = confirmation of adding exchange or error.

* Get All Exchanges: <br />
   Return = JSON of all exchanges (hyperlink to Design of master dataset)

* Remove exchange: <br />
    Params: Exchange name. <br />
    Return: Message confirming the change.

* Clear all list: Clears the dataset of all exchanges to start from scratch. <br />
    Return: confirmation message.

**Ordering of Data:**

* Holdings <br />
Transactions ordered by coins <br />
Title of set is ordered by total of current price of holdings of the coin <br />
Ordered Alphabetically <br />
The GET request returns the data <br />

* Chronological <br />
Transactions ordered chronologically <br />
Can be used to display overall growth of portfolio. <br />
Title set is ordered by Month, Week, and Day <br />
The GET request returns the data
