# Get Latest Charity Campaign
Fetches your latest Twitch Charity campaign and adds the information as variables
:image-preview

## Variables
:variables-description

Name | Description | Example
----:|:------------|---------|
`campaignId` | Twitch's internal ID for your campaign.
`charity.name` | The name of the charity you are supporting.
`charity.description` | The description of the charity you are supporting.
`charity.logoUrl` | The logo of the charity you are supporting.
`charity.websiteUrl` | The website to the charity you are supporting.
`currentAmount` | How much you have raised so far, in cents | `4200`
`targetAmount` | Your campaign's target amount, in cents | `5000`

## C# Usage
:csharp-method