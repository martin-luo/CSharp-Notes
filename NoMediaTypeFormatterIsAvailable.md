# Detailed Error Message
"No MediaTypeFormatter is available to read an object of type 'FormDataCollection' from content with media type 'multipart/form-data'."

# Basic Info about the Context
- Language Version: C# 4.6.1
- Controller Type: `ApiController`
- Method invoked: `Request.Content.ReadAsFormDataAsync()`

# Why It Happened?
I used the the method the "ReadAsFormDataAsync" method to read the FormData from the request content, which only accepts "application/x-www-form-urlencoded" type of contents. It doesn't support get the 'multipart/form-data' type of contents, which is the type of my request content.

# Solution I found
I installed the a parser to parse the multipart data.

The parser I used is called [Http-Multipart-Data-Parser](https://github.com/Http-Multipart-Data-Parser/Http-Multipart-Data-Parser).

# Acknowledgement
- [Stackoverflow - No MediaTypeFormatter is available to read an object of type 'HttpRequestMessage' from content with media type 'multipart/form-data'](https://stackoverflow.com/questions/45949830/no-mediatypeformatter-is-available-to-read-an-object-of-type-httprequestmessage)
- [Stackoverflow - Are there any multipart/form-data parser in C# - (NO ASP)](https://stackoverflow.com/questions/3880530/are-there-any-multipart-form-data-parser-in-c-sharp-no-asp)
- [Stackoverflow - Parsing “multipart/form-data” in .NET/C#](https://stackoverflow.com/questions/1716868/parsing-multipart-form-data-in-net-c/1718859#1718859)
- [Stackoverflow - Reading file input from a multipart/form-data POST](https://stackoverflow.com/questions/7460088/reading-file-input-from-a-multipart-form-data-post)
- [Stackoverflow - ASP.NET How read a multipart form data in Web API?](https://stackoverflow.com/questions/40632028/asp-net-how-read-a-multipart-form-data-in-web-api?rq=1
)
