Hi,
This Blazor component for checking differences between to Json files.

![image](https://github.com/user-attachments/assets/c831adbc-0e25-4002-b2e4-5069896653e7)

This is sample code:
```cshtml
@using JsonDiffsBlazorComponent
@page "/"

<PageTitle>JsonDiffs</PageTitle>

<JsonDiffs FirstJson=@Json1 SecondJson=@Json2></JsonDiffs>
@code{
    public string Json1 { get; set; } = "{\"companyName\":\"TechInnovatorsInc.\",\"founded\":2010,\"isActive\":true,\"employees\":[{\"name\":\"JohnDoe\",\"age\":30,\"skills\":[\"JavaScript\",\"Python\",\"HTML\"]},{\"name\":\"JaneSmith\",\"age\":25,\"skills\":[\"Java\",\"SQL\",\"CSS\"]}],\"projects\":[{\"title\":\"MobileAppDevelopment\",\"budget\":15000,\"deadline\":\"2026-03-15\"}],\"headquarters\":{\"city\":\"NewYork\",\"country\":\"USA\",\"contact\":{\"email\":\"info@techinnovators.com\",\"phone\":\"+1-555-1234\"}}}";
    public string Json2 { get; set; } =  "{\"companyName\":\"TechInnovatorsInc.\",\"founded\":2010,\"isActive\":true,\"employees\":[{\"name\":\"JohnDoe\",\"age\":30,\"skills\":[\"C#\",\"Python\",\"HTML\"]},{\"name\":\"\",\"age\":25,\"skills\":[\"Java\",\"SQL\",\"CSS\"]}],\"projects\":[{\"title\":\"WebsiteRedesign\",\"budget\":5000,\"deadline\":\"2025-12-01\"},{\"title\":\"MobileAppDevelopment\",\"budget\":15000,\"deadline\":\"2026-03-13\"}],\"headquarters\":{\"city\":\"Athens\",\"country\":\"Greece\",\"contact\":{\"email\":\"info@techinnovators.com\",\"phone\":\"+1-555-1234\"}}}";
}
