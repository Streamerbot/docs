```cs
public class TeamInfo
{
    public string Id { get; set; }
    public string Name { get; set; }
    public string Login { get; set; }
    public string BackgroundImageUrl { get; set; }
    public string Banner { get; set; }
    public string CreatedAt { get; set; }
    public string UpdatedAt { get; set; }
    public string Info { get; set; }
    public string ThumbnailUrl { get; set; }
    public string TeamName { get; set; }
    public string TeamDisplayName { get; set; }
    public string TeamId { get; set; }
}
```

The TeamInfo list is indexed, meaning it starts with `0` for the first team in the list.

Example:
```cs
var teamInfo = CPH.GetTeamInfo("lyfesaver74");
CPH.LogInfo(teamInfo[0].TeamName);
```
