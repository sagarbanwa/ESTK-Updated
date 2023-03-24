# ESTK-Updated
Elasticsearch Mod and updated version  

# ES Toolkit
# updated Version 


[![GitHub Release](https://img.shields.io/github/v/release/LeakIX/estk)](https://github.com/LeakIX/estk/releases)
[![Follow on Twitter](https://img.shields.io/twitter/follow/leak_ix.svg?logo=twitter)](https://twitter.com/leak_ix)

ES ToolKit is a standalone solution to navigate and backup data for a 
wide range of Elasticsearch and Kibana versions.

## Features

- Automatic software and version detection
- Query support
- Low memory/CPU footprint
- Dump directly to file or stdout
- Live progress
- Proxy support

## Usage

### List index

```
estk list -h
```

Displays help for the list command.

|Flag           |Description  |
|-----------------------|-------------------------------------------------------|
|--url     | Elasticsearch/Kibana root URL |

### Dump index

```
estk dump -h
```

Displays help for the dump command.

|Flag           |Description  |
|-----------------------|-------------------------------------------------------|
|--url     | Elasticsearch/Kibana root URL |
|--index     | Name of the index to dump ( wildcard supported ) |
|--query-string | Dump specific documents |
|--size| Bulk size, max amount of document per request|

## Installation Instructions

### From Binary

The installation is easy. You can download the pre-built binaries for your platform from the [Releases](https://github.com/LeakIX/estk/releases/) page.

```sh
▶ chmod +x estk-linux-64
▶ mv estk-linux-64 /usr/local/bin/estk
```

### From Source


```sh
▶ GO111MODULE=on go get -u -v github.com/LeakIX/estk
▶ ${GOPATH}/bin/estk -h
```

## Running estk

```sh
▶ estk --url http://127.0.0.1:5602 dump -i "hostserviceleak" -o hostserviceleak.json -d -q "type:mysql"
2020/12/16 20:12:15 Detecting version...
2020/12/16 20:12:15 Trying elasticsearch
2020/12/16 20:12:15 Trying Kibana
2020/12/16 20:12:15 Found kibana, major version 7
2020/12/16 20:12:15 Dump starting...
2020/12/16 20:12:15 Endpoint : http://127.0.0.1:5602
2020/12/16 20:12:15 Index : hostserviceleak
2020/12/16 20:12:15 Output file : hostserviceleak.json
2020/12/16 20:12:16 Got scrollId : FGluY2x1ZGVfY29udGV4dF91dWlkDnF1ZXJ5VGhlbkZldGNoAhRLRVQzYkhZQnowRHZjdlFkblNHWgAAAAABlhWbFnpNNWpoU3RhUk5Td3hCVXAxd1k2TUEUS1VUM2JIWUJ6MER2Y3ZRZG5TR1oAAAAAAZYVnBZ6TTVqaFN0YVJOU3d4QlVwMXdZNk1B
2020/12/16 20:12:16 Dumping 2292659 documents :
   1% |                                                    | (34201/2292659, 242 it/s) [2m23s:2h35m22s]
```

### HotFix Done " Dump any data even which start with . or .products .(ptoducts) .. etc"
## Modded 

```sh
git clone https://github.com/sagarbanwa/ESTK-Updated.git
cd ESTK-Updated
go build 
```


### This tool is modifed from LeakIX and more update recevied by him not from me as he is the owner of the tool.
