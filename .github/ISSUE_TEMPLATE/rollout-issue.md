---
name: Rollout issue
about: Create issue to capture rollout audit trail
title: ''
labels: Rollout
assignees: ''

---

The purpose of this issue is to keep track of this repository rollouts. It should be used to link all issues encountered during a rollout and their resolution to keep full audit trail of rolled out changes.

# Process

Rollout preparation (Monday)
- [ ] Check the status of the [dotnet-arcade-services-weekly](https://dev.azure.com/dnceng/internal/_build?definitionId=993) pipeline
- [ ] Ensure the [arcade-services-internal-ci](https://dev.azure.com/dnceng/internal/_build?definitionId=252) pipeline is green
- [ ] Synchronize on the [Rollout channel](https://teams.microsoft.com/l/channel/19%3a72e283b51f9e4567ba24a35328562df4%40thread.skype/Rollout?groupId=147df318-61de-4f04-8f7b-ecd328c256bb&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) on rolling out this week
Prepare the release notes
- [ ] Merge the rollout PR prepared by the vendor
- [ ] Ensure the build is green and stops on the "Approval" phase

On rollout day (Wednesday)
- [ ] Approve the rollout build
- [ ] Ensure the rollout is finished
- [ ] Link all issues encountered during the rollout to this issue
- [ ] Update the rollout stats in the "Stats" section below
- [ ] Notify the [Rollout channel](https://teams.microsoft.com/l/channel/19%3a72e283b51f9e4567ba24a35328562df4%40thread.skype/Rollout?groupId=147df318-61de-4f04-8f7b-ecd328c256bb&tenantId=72f988bf-86f1-41af-91ab-2d7cd011db47) and close this issue

# Rollout stats

Use the following Kusto query to fill in the rollout stats below:

Pre-Approval run time: `<FILL>`
Post-Approval run time: `<FILL>`

# Useful links

- [Production build runs](https://dev.azure.com/dnceng/internal/_build?definitionId=252&_a=summary&branchFilter=10418%2C10418%2C10418%2C10418)
- [Kusto query for duration](https://dataexplorer.azure.com/clusters/engsrvprod/databases/engineeringdata?query=H4sIAAAAAAAAA51Ry07DQAy85yusXEiq0EIPIBr1QJWqVEJQtcAFoWpJ3GbRPqJdhzf/jhMKChzZkzX2zHi8CgmWVilb07yAMQx6k+v5eQbzDGaX0xWcTZfTBLC/7cNweHhwcnTcG6SBYtYMKaudIGkN86K1LEagrNkmsN5I52lFYosj8ORkCyrxB4vhLQB+V1KjkgaXmFtX+BZ7h6cSHcKklqpoFhsDG/xqXQiNIE3Uceu6xLthX2stnHxFdhWOeFXNpFVTN8YxhzNNcC2eO+iOXDn7gDlBJ+jGOi1oTTzlK2Gihr3/pZ1AWJYjrcM4DT7SoOKQ1Ard7i0cnlas9igURO1QvHfHamR9LpRwUeea0c9/sGB7gJCLRX2vpC+h9nw6yITLwzhOvuWtp//pZ1gp+9IY3AglC0EIRQtpNMQO6SfbzDU/IQIAAA==)
- [Maestro exceptions](https://ms.portal.azure.com/#view/Microsoft_OperationsManagementSuite_Workspace/Logs.ReactView/resourceId/%2Fsubscriptions%2F68672ab8-de0c-40f1-8d1b-ffb20bd62c0f%2FresourceGroups%2Fmaestro-prod-cluster%2Fproviders%2Fmicrosoft.insights%2Fcomponents%2Fmaestro-prod/source/LogsBlade.AnalyticsShareLinkToQuery/q/H4sIAAAAAAAAAz2MOw6DMBBE%252B5xiSlsiRZDS5i7GjGQXu0brRSSIwyekoH4fvjMXr0377cBWaIRXYfckC17QtoV4H%252Bcf7KtIsroTua3qIWL6YKoaLn%252FA4ylxgNBLOxOjzrT%252FMJdk%252FgV08ryabQAAAA%253D%253D)
