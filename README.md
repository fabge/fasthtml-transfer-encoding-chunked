# fasthtml-sse

This example implements a chatbot. Most parts are copied from the [fasthtml chatbot example](https://github.com/AnswerDotAI/fasthtml-example/blob/main/02_chatbot/README.md).  

However instead of using websockets, this example uses [**`Transfer-Encoding: chunked`**](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers/Transfer-Encoding#chunked_encoding) which allows streaming of content without long lived connections.

As the connection to the server is terminated after every message, the server only needs to be running a couple of (milli-)seconds, enabling deployments using serverless functions like AWS Lambda or Azure Functions.
