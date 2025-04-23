# Guided SAM tips

## Checking a SAM templates Validatey

To validate a SAM template, we can use the command:

```
    sam validate
```

This will produce an informative output of whether the reported template is sufficent or not

---

## Checking an API Gateways endpoints

To manually check for API Gateway APIs that exist on an account, we can do:
```
    aws apigatewayv2 get-apis
```

This will produce an array of `Items` that should have an `ApiId` associated with the relevant API Gateway on the account. Using this, we can then run the below command:
```
    aws apigatewayv2 get-routes --api-id <your-api-id>
```

The follow command will allow for us to manually verify what API route exist on the Gateway. For example, a root level api `/`, or something more like `/admin`.