# Bash client Library for the Brainrex API

Welcome to the Brainrex API explorer, we make analytics tools for crypto and blockchain. Our currently propiertary models offer sentiment analysis, market making, blockchain monitoring and face-id verification. This AI models can be consumed from this API. We also offer integrations to open data and propietary data providers, as well as free test data we collect. There is a collection of data transformation tools. Join our Telegram group to get the latest news and ask questions https://t.me/brainrex, #brainrex. More about Brainrex at https://brainrex.com. Full Documentation can be found at https://brainrexapi.github.io/docs
## Overview
This is a Bash client script for accessing Brainrex API Explorer service.

The script uses cURL underneath for making all REST calls.

## Usage

```shell
# Make sure the script has executable rights
$ chmod u+x

# Print the list of operations available on the service
$ ./ -h

# Print the service description
$ ./ --about

# Print detailed information about specific operation
$ ./ <operationId> -h

# Make GET request
./ --host http://<hostname>:<port> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make GET request using arbitrary curl options (must be passed before <operationId>) to an SSL service using username:password
 -k -sS --tlsv1.2 --host https://<hostname> -u <user>:<password> --accept xml <operationId> <queryParam1>=<value1> <header_key1>:<header_value2>

# Make POST request
$ echo '<body_content>' |  --host <hostname> --content-type json <operationId> -

# Make POST request with simple JSON content, e.g.:
# {
#   "key1": "value1",
#   "key2": "value2",
#   "key3": 23
# }
$ echo '<body_content>' |  --host <hostname> --content-type json <operationId> key1==value1 key2=value2 key3:=23 -

# Preview the cURL command without actually executing it
$  --host http://<hostname>:<port> --dry-run <operationid>

```

## Docker image
You can easily create a Docker image containing a preconfigured environment
for using the REST Bash client including working autocompletion and short
welcome message with basic instructions, using the generated Dockerfile:

```shell
docker build -t my-rest-client .
docker run -it my-rest-client
```

By default you will be logged into a Zsh environment which has much more
advanced auto completion, but you can switch to Bash, where basic autocompletion
is also available.

## Shell completion

### Bash
The generated bash-completion script can be either directly loaded to the current Bash session using:

```shell
source .bash-completion
```

Alternatively, the script can be copied to the `/etc/bash-completion.d` (or on OSX with Homebrew to `/usr/local/etc/bash-completion.d`):

```shell
sudo cp .bash-completion /etc/bash-completion.d/
```

#### OS X
On OSX you might need to install bash-completion using Homebrew:
```shell
brew install bash-completion
```
and add the following to the `~/.bashrc`:

```shell
if [ -f $(brew --prefix)/etc/bash_completion ]; then
  . $(brew --prefix)/etc/bash_completion
fi
```

### Zsh
In Zsh, the generated `_` Zsh completion file must be copied to one of the folders under `$FPATH` variable.


## Documentation for API Endpoints

All URIs are relative to */api*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BlockchainApi* | [**blockchain.averageTx**](clients/bash/docs/BlockchainApi.md#blockchain.averagetx) | **POST** /average_tx_fee | Calculate average transccion fee of a given blockchain
*BlockchainApi* | [**blockchain.list**](clients/bash/docs/BlockchainApi.md#blockchain.list) | **GET** /list_blockchain | The blockchains data structure supported by the Brainrex API
*CryptoApi* | [**exchanges.downloadCandles**](clients/bash/docs/CryptoApi.md#exchanges.downloadcandles) | **POST** /download_candles | Downloads candle format market data
*CryptoApi* | [**exchanges.list**](clients/bash/docs/CryptoApi.md#exchanges.list) | **GET** /markets | The markets data structure supported by the Brainrex Market API
*CryptoApi* | [**exchanges.marketmaker**](clients/bash/docs/CryptoApi.md#exchanges.marketmaker) | **POST** /market_making | Market Making as a Service API.
*CryptoApi* | [**exchanges.read**](clients/bash/docs/CryptoApi.md#exchanges.read) | **GET** /exchanges | The exchanges data structure supported by the Brainrex API
*CryptoApi* | [**exchanges.tickerDataDownload**](clients/bash/docs/CryptoApi.md#exchanges.tickerdatadownload) | **POST** /download_ticker | Download raw ticker data from major crypto markets
*SentimentAnalysisApi* | [**sentiment.getPriceSentiment**](clients/bash/docs/SentimentAnalysisApi.md#sentiment.getpricesentiment) | **POST** /get_buy_sentiment | Sentiment analysis score using a model trained for buy signals.
*SentimentAnalysisApi* | [**sentiment.getSentiment**](clients/bash/docs/SentimentAnalysisApi.md#sentiment.getsentiment) | **POST** /get_sentiment | Sentiment analysis for any given blob of text


## Documentation For Models

 - [Inline_response_200](clients/bash/docs/Inline_response_200.md)
 - [Inline_response_200_1](clients/bash/docs/Inline_response_200_1.md)
 - [Inline_response_200_2](clients/bash/docs/Inline_response_200_2.md)
 - [Inline_response_201](clients/bash/docs/Inline_response_201.md)
 - [Inline_response_201_1](clients/bash/docs/Inline_response_201_1.md)
 - [Request](clients/bash/docs/Request.md)
 - [Request_1](clients/bash/docs/Request_1.md)
 - [Request_2](clients/bash/docs/Request_2.md)
 - [Request_3](clients/bash/docs/Request_3.md)
 - [Text](clients/bash/docs/Text.md)
 - [Text_1](clients/bash/docs/Text_1.md)


## Documentation For Authorization

 All endpoints do not require authorization.
