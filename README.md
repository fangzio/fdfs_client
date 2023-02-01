<center>
<h3>FastDfs Client</h3>
</center>
<hr/>
fastDfs client is a an MIT-licensed open source project, which is implemented by golang.

## Implement
```
//upload by filename
UploadByFilename

//upload by buffer
UploadByBuffer

//download by fileId to local file
DownloadToFile

//download by fileId to buffer
DownloadToBuffer

//delete by fileId
DeleteFile
```

## Import
```bash
go get code.sohuno.com/sky/fdfs_client
```

## Use
```go
hosts = strings.Split(ServerConfig.Fdfs.ServerAddr, ",")
client, err := fdfs_client.NewClientWithConfig(hosts, ServerConfig.Fdfs.MaxConn)

data, err = os.ReadFile("./abc.jpg")
fileId, err = client.UploadByBuffer(data, "jpg")
```

## License
MIT

Copyright (c) 2022-present, Sohu ltd