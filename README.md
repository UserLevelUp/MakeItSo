# 🖖 MakeItSo: Simple & Reliable File Management for .NET, Inspired by Star Trek LCARS

## What is MakeItSo?

**MakeItSo** helps you safely create, organize, and track files and logs in your .NET applications. Inspired by Star Trek's LCARS computer system, it makes file engagement easy, reliable, and even fun—**engaging maximum warp** for your development workflow.

---

## Why Use MakeItSo?

- **Red Alert: No More Lost Files!**  
  Uses a proven "ADD/DEL" safeguard to make sure your files and logs are never accidentally deleted or overwritten—your data is **safe at warp speed**.

- **Easy Tracking with **Stellar** Navigation**  
  Automatically creates organized files and log entries, so you can always see what happened and when—like having **Data** manage your file systems.

- **Beautiful Reports from the **Bridge****  
  Gives you simple and colorful health checks, showing if your files and logs are safe and working—just like Star Trek's **LCARS computer screens**.

- **Plug & Play **Universal Translator****  
  Works with regular files, cloud storage (like Azure or AWS), and even databases (like SQLite)—all with the same easy setup across the **galaxy**.

- **Custom Suffix Workflows: **Prime Directive** Flexibility**  
  Go beyond just "_add" and "_del"—define your own file suffixes and workflows (such as "_archive", "_backup", "_error", and more) to fit your **mission parameters**.

---

## How Does It Make Life Simpler?

- **Just Add a Line: **One to Beam Up****  
  With one line of code, you get safe file creation and logging—**energize!**
- **Automatic Safety: **Shields Up****  
  Prevents mistakes when multiple users or programs access your files at the same time—**deflector shields** for your data.
- **Instant Status: **Tricorder** Readings**  
  Run a check and instantly see if everything is OK—no more digging through folders or error logs. **"Fascinating, Captain."**
- **Flexible: **Holodeck** Versatility**  
  Track work, app events, or logs—whatever you need! **Computer, arch.**
- **Custom Workflows: **Replicator** Technology**  
  Set up new suffixes and actions for your files, so your workflow matches exactly what your **crew** needs.

---

## Example: Logging an Event (**Captain's Log**)

```csharp
await lcars.WriteAsync("logs", "User signed in");
// This safely adds a log entry, using the ADD/DEL pattern to avoid errors.
// "Captain's log, stardate 2025.249..."
```

## Example: Custom Suffix Workflow (**Engineering** Specifications)

```csharp
// Register a custom suffix for files marked as "archived"
options.SuffixConfiguration.RegisterCustomSuffix("archive", fileName => $"{fileName}_archive_{DateTime.Now:yyyyMMdd}");
```
*You can create custom suffixes for archiving, backups, errors, or any workflow you need—**"I'm givin' her all she's got, Captain!"***

## Example: Checking Health (**Medical** Tricorder)

```csharp
var report = await lcars.RunDiagnosticsAsync();
Console.WriteLine(report.GetLCARSDisplay());
```
*See a colorful status—green means good, yellow or red means check your files! **"He's dead, Jim... but your files are fine!"***

---

## Getting Started (**Setting Course**)

1. **Install the package: **Beam Down** from NuGet**
   ```bash
   dotnet add package UserLevelUp.MakeItSo.LCARS
   ```

2. **Configure and use: **Engage** Systems**
   ```csharp
   builder.Services.AddLCARSFileSystem(options =>
   {
       // Example: add custom suffix workflows
       options.SuffixConfiguration.RegisterCustomSuffix("backup", fileName => $"{fileName}_backup");
   });
   ```

3. **Start tracking, logging, and customizing your workflow! **Set course** for success!**

---

## Who is it for? (**Crew** Manifest)

- Developers who want **easy, safe logging and file tracking** (**Starfleet Academy** graduates)
- Teams that need **organized work records and event logs** (**Bridge crew** coordination)
- Anyone building .NET apps—big or small! (**Federation** or **Independent** colonies)
- Anyone who wants to customize how their files are named and managed (**Chief Engineers**)

---

## License (**Federation** Charter)

Open source under MIT License—free for everyone across the **Alpha Quadrant**!

---

**MakeItSo: The simple, safe way to manage and track your files and logs—with custom workflows. Live long and prosper! 🖖**

*"Number One, engage the file management system!"*