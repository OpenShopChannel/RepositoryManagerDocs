# FAQ

### How long does it take for an application or update to show up on the repository?

If you've recently updated your application and the repository can still retrieve it correctly using the application manifest located at [OpenShopChannel/Apps](https://github.com/OpenShopChannel/Apps), your update will be automatically added to the repository. However, this process can take some time.

Currently, the Repository Manager checks all applications four times a day, with each check happening every 6 hours. Please note that this schedule may change in the future.

Here's a simplified breakdown of how an application update gets added:

1. Repository Manager starts its regular check.
2. During this check, if it detects that there's an update available for an application, it sends the update for moderation. The old version of the app remains available for now.
3. Repository Manager completes its check.
4. It then starts another regular check.
5. During this check, if there's an update, it checks the moderation status. If the update passes moderation, it gets applied; otherwise, it's skipped.
6. If the update detected in the previous check was removed by this point, the update won't be added.
7. Repository Manager finishes its check. If the update was approved by moderation, it becomes available in the repository.

If the moderation process is fast, it can take two regular checks, which is roughly 12 hours, to process an update.

However, if there are issues with applying the update, like changes in the archive's directory structure that the Repository Manager can't handle automatically, it will need manual fixing, which may take much longer.
