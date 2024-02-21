🧠 Classes with Only Variables => Blurprint / Data Structures / Data Schemas:
   - Classes that consist only of variables and no methods are often used to represent data structures or models, especially in frameworks that work with data serialization and validation (like Pydantic in the `APIGatewayProxyEventModel` case).
   - These classes serve as a blueprint for creating objects with a specific structure, ensuring consistency and facilitating data handling. They can also include validation, serialization, and deserialization logic, which is often handled by the parent class or framework (like `BaseModel` in Pydantic).
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
