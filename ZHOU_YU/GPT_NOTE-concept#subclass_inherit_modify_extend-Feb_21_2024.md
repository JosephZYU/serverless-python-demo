🧠 Parent-Class -> Class -> Sub-Class:
- [Python OOP Tutorial 4: Inheritance - Creating Subclasses](https://youtu.be/RSl87lqOXDE?si=nH9df-ddTitcarD-):
- Use class inheritance to auto-embed ALL variables from preceding/upper-level to modify/over-write/extend
- the `CreateProductRequest` class extends the `APIGatewayProxyEventModel` class by adding specific attributes (`body` and `pathParameters`) that define the expected structure of an API Gateway event for a product creation request. This structure is essential for handling API requests in a consistent and predictable manner, especially in serverless applications where data validation and serialization are crucial.
    ```py
    class APIGatewayProxyEventModel(BaseModel):
        version: Optional[str] = None
        resource: str
        path: str
        httpMethod: Literal["DELETE", "GET", "HEAD", "OPTIONS", "PATCH", "POST", "PUT"]
        headers: Dict[str, str]
        multiValueHeaders: Dict[str, List[str]]
        queryStringParameters: Optional[Dict[str, str]] = None
        multiValueQueryStringParameters: Optional[Dict[str, List[str]]] = None
        requestContext: APIGatewayEventRequestContext
        pathParameters: Optional[Dict[str, str]] = None
        stageVariables: Optional[Dict[str, str]] = None
        isBase64Encoded: bool
        body: Optional[Union[str, Type[BaseModel]]] = None
    ```
    ```py
    # Define a custom model extending APIGatewayProxyEventModel
    class CreateProductRequest(APIGatewayProxyEventModel):
        body: Optional[PutProduct]  # type: ignore
        pathParameters: Optional[Dict[str, str]]  # type: ignore
    ```
   - In the `CreateProductRequest` class, redefining `body: Optional[PutProduct]` overrides/replaces the definition of `body` in the parent `APIGatewayProxyEventModel` class. It does not alter the parent class definition itself. This change affects only the `CreateProductRequest` class and any classes derived from it, not the `APIGatewayProxyEventModel` class or its other subclasses.
   - This means the `body` attribute in `CreateProductRequest` will specifically expect a `PutProduct` type, not just any string or `BaseModel` as defined in the parent class. This is a way of extending and specifying the functionality for the specific use case of `CreateProductRequest`.
   - In object-oriented programming, this is a common practice where derived classes refine or override attributes and methods from their parent classes to fit specific needs.
   - Indeed, attributes in Python are case-sensitive. To override an attribute from a parent class, you must use the exact attribute name, matching its case. In the context of inheritance, matching the attribute name precisely is crucial for proper overriding behavior.
