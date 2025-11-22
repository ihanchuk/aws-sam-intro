#### Cloud Formation краткое введение

##### Минималистичный пример шаблона, описывающий создание S3

Этот шаблон создаст минимальный S3 без имени, настроек и тп

``` Yaml
Resources:
    MyDemoBucket:
        type: AWS::S3::Bucket
```

А теперь слегка усложним - добавим параметр для имени нашего бакета

``` Yaml
Parameters:
  MyBucketNameParameter:
    Type: String
    Description: This is how the bucket will be called

Resources:
  MyDemoBucket:
    Type: AWS::S3::Bucket
    Properties:
      BucketName: !Ref MyBucketNameParameter
```


