Generics make it so a method or class can be used by several different types.
```
 public class ApiGatewayClient<T>
    {
        public async Task<T> PostAsync(string urlPath, T payload)
        {
            var fullUri = new Uri(apiBaseUri, urlPath);

            HttpRequestMessage httpRequestMessage = PrepareHttpRequestMessage(payload, fullUri, HttpMethod.Post);

            var response = await retryPolicy.ExecuteAsync(async () => await client.SendAsync(httpRequestMessage)
            .ConfigureAwait(false))
                .ConfigureAwait(false);

            if (!response.IsSuccessStatusCode)
            {
                throw new HttpResponseException(response.StatusCode);
            }

            var content = await response.Content.ReadAsStringAsync();

            var responseObject = JsonConvert.DeserializeObject<T>(content);

            return responseObject;

        }
    }
    ```
