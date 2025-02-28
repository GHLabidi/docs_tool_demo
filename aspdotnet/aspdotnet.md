
# ASP.NET Core Documentation 🚀

## 🏗️ How to Start a New Project
To create a new ASP.NET Core project, use the following command:

```sh
dotnet new webapp -n MyAspApp
cd MyAspApp
dotnet run
```
This creates a new web application and runs it locally.

---

## 🎯 How to Create a Controller
Controllers handle HTTP requests in ASP.NET Core. To create a new controller:

1. Navigate to the `Controllers` folder.
2. Create a new file `MyController.cs`:

```csharp
using Microsoft.AspNetCore.Mvc;

[ApiController]
[Route("api/[controller]")]
public class MyController : ControllerBase
{
    [HttpGet]
    public IActionResult Get()
    {
        return Ok("Hello from ASP.NET Core!");
    }
}
```

3. Run the application and test the API:  
   ```
   https://localhost:5001/api/mycontroller
   ```

---

## 🔐 Setting Up Authentication with Attributes
ASP.NET Core provides **authorization attributes** to protect endpoints.

1. Enable authentication in `Program.cs`:

```csharp
builder.Services.AddAuthentication(JwtBearerDefaults.AuthenticationScheme)
    .AddJwtBearer(options => {
        options.Authority = "https://your-auth-provider.com";
        options.Audience = "your-api";
    });
```

2. Protect controllers with `[Authorize]`:

```csharp
using Microsoft.AspNetCore.Authorization;

[Authorize]
[ApiController]
[Route("api/protected")]
public class ProtectedController : ControllerBase
{
    [HttpGet]
    public IActionResult GetSecret()
    {
        return Ok("🔒 This is a protected endpoint.");
    }
}
```

Now, only authenticated users can access `/api/protected`. ✅
