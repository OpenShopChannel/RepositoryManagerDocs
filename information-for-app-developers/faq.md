# FAQ

### How long does it take for an application/update to be added or applied?

If you updated your application, and the manifest for the application located on the [OpenShopChannel/Apps](https://github.com/OpenShopChannel/Apps) repository can still correctly retrieve it, then the application will be automatically updated on the repository.

This can take a while. As of writing, Repository Manager indexes all applications 4 times a day, once per 6 hours. This might change in the future.

The flow for an application update looks like this:

* Repository Manager starts a regularly scheduled re-index.
* While trying to retrieve the application, it determines that there has been an update.
* Application is submitted to moderation. For the time being, the prior version of the app is kept available.
* Repository Manager finishes re-index.
* Once again, Repository Manager starts a regularly scheduled re-index.
* While trying to retrieve the application, it determines that there has been an update.
* Checks moderation status for this specific update. If passed, update the application. Otherwise, continue skipping it.\
  **If the application update detected during the previous re-index was pulled by this point, then the update will not be applied.**
* Repository Manager finishes re-index. **At this point, if the application/update was approved by moderation, it is available on the repository.**

If moderation is quick to approve an update, then it will take two regularly scheduled indexings to process an update, or up to around 12 hours.

If there are issues with applying the update, for example, the directory structure in the distributed archive has changed and Repository Manager can no longer successfully process it, then the manifest will require manual fixing, and this may take much longer.
