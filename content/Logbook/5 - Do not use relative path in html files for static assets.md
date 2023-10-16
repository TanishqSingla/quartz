16th July 2023, Sunday

## Overview

Today I was working on creating a draft PR for adding tests for task-requests feature on website-dashboard for RDS. I felt really tired in the day and my brain wasn’t working on a very good capacity.  
So nights was it where I resolved some issues that I encountered with prettier and jest, which I later tweeted about ofc. Here are the tweets in case my twitter data is suddenly lost

- Got stuck due to mistakes while using Node.js, Puppeteer and Jest, while working on website-dashboard of [@RealDevSquad](https://twitter.com/RealDevSquad). The worst part was the lack of resources on stackoverflow as well as puppeteer guides.  
    Here's a heads up if you guys are doing these mistakes too.
- Mistake 1 - Using relative paths for loading assets. I prefer relative paths in my workflow and most server implementations also supports it, so I assumed jest-puppeteer also did, and lo it didn't.
- Mistake 2 - Not closing the puppeteer browser properly.  
    I forgot to add await before browser.close() which led the browser running on the port that was specified in the config. Apparently jest wasn't able to kill the process on its own too.
- Mistake 3 - Not using sudo to find the right pid of the browser.  
    This might be the reason why the process was not killed by jest automatically. I used `lsof -t -i :8000` to kill the process but failed every time as the process would be killed but localhost: was working.

## Conclusion

I now believe my assumption to use relative path was very wrong and should always resort to using absolute paths.