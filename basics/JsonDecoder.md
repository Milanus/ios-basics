# JsonDecoder

> customize json decoder from  camel case to snake case 

```
static let jsonDecoder: JSONDecoder = {
       let jsonDecoder = JSONDecoder()
       jsonDecoder.keyDecodingStrategy = .convertFromSnakeCase
       jsonDecoder.dateDecodingStrategy = .formatted(dateFormatter)
       return jsonDecoder
 }()

```