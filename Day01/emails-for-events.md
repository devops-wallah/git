# How Users Receive Emails for GitHub Events

- Note: [Github Email Service](https://docs.github.com/en/enterprise-server@3.16/admin/configuring-settings/configuring-user-applications-for-your-enterprise/configuring-email-for-notifications)

## In GitHub, users receive email notifications for events such as: Pull Request (PR) creation, Requested changes, Comments on PRs or issues, Mentions (@username), PR approvals
- When any of these events occur, GitHub generates a notification event. This event is then processed by GitHub’s notification service, which determines the users who should be notified based on:  Repository watch settings, Participation in the PR/issue, Mentions, Notification preferences

- GitHub then sends the notification through its email service to the corresponding email addresses.

## For GitHub Enterprise Server, administrators must configure an SMTP server to enable email delivery. This configuration typically includes:

- SMTP server URL/hostname, Port number, TLS/SSL configuration, Authentication credentials (if required), A no-reply email address (e.g., noreply@company.com)

- Once configured, GitHub uses the SMTP server to send notification emails to users for repository events.