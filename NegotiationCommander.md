
# TO DO
## Handler
* SC-1.5. Обработка решения клиента (кейсы send и verify)
	
## HumanTask
* smth

## Rules Engine
| event | type | result | desc |
| ------ | ----------- | ----------- | ------- |
| scoring   | approved | negotiation-recalculation | окончание скоринга, идем на rbp |
| recalculation   | approved | negotiation-customerDesicion | получить решение клиента |
| recalculation |  denied | terminator-deny  |  нет предложений |
| customerDesicion   | received | negotiation-desicionAnalysis| обработать решение клиента |
| negotiation   | completed | ? | окончание Нег |


## Table of Contents
  * [Chapter 1](#chapter-1)

This is [an example](http://www.example.com/) inline link.


# BULK API

Google Request: "restfull service POST a group of resources".


* https://cloud.google.com/appengine/docs/standard/java/microservice-performance
* [Implementing bulk updates within RESTful services](http://restlet.com/company/blog/2015/05/18/implementing-bulk-updates-within-restful-services/)


* [Publishing a multi-photo post with uploaded photos](https://developers.facebook.com/docs/graph-api/photo-uploads#upload) - о том, как FB реализует загрузку пачки фотографий (используется два сервиса)
* [Google Drive API Reference](https://developers.google.com/drive/api/v3/reference/)

* [Sending binary data along with a REST API request](http://blog.marcinbudny.com/2014/02/sending-binary-data-along-with-rest-api.html)
### multipart/form-data
In some cases, maybe for compatibility reasons, you’ll not be able to use modern binary serialization like BSON or protobuf. In those cases you can still avoid sending binary data in BASE64 encoded string. You can use multipart/form-data request, effectively simulating HTML forms with file uploads behavior. This is a bit more complex than the previous approaches, so I would like to go into more detail.

But before that, I should mention, that this approach is not semantically correct. By using the Content-Type multipart/form-data you state, that what you send is actually a form. But it is not. It is rather some custom data format and for that, the most appropriate content type seems to be multipart/mixed (see the RFC). The HttpClient library for .NET won’t have any problems handling different subtypes of multipart/* MIME type, but for other platforms, it may not be true. I have seen some libraries (for Python for example), which had multipart/form-data content type hardcoded. So in this case you have two options: either write your own client library or give up being semantically correct and go with multipart/form-data. I can live with the latter.

* [Implementing bulk updates within RESTful services](http://restlet.com/company/blog/2015/05/18/implementing-bulk-updates-within-restful-services/)

* [](https://stackoverflow.com/questions/33279153/rest-api-file-ie-images-processing-best-practices)

* [What is Considered a Single Microservice?](https://codeburst.io/what-is-considered-a-single-microservice-74cd6353b886)

* [RESTful API design : Microservices](https://medium.com/@cknextmove/restful-api-design-microservices-f983e3ea3563)

* [](https://code.tutsplus.com/tutorials/wp-rest-api-creating-updating-and-deleting-data--cms-24883)

## markable
* [Transfering multiple files and meta data in POST request](https://stackoverflow.com/questions/48308464/transfering-multiple-files-and-meta-data-in-post-request)

* [Reading and Writing Multiple Documents](https://docs.marklogic.com/guide/rest-dev/bulk) Содержит много примеров реализации.










