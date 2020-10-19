IT IS NECESSARY TO PAY ATTENTION TO THE WAY THE PAGINATION WAS PERFORMED

As long as youtube has changed its approach in assigning pageToken in its lates v3 release, the process of url configuration set up, that's obviously a mandatory to be performed each time a new page is being assigned with new token, has become rather complicated. Basically you have to update your url each time a page token is assigned and have that url fetched afterwards.

However I noticed that Youtube basically use same pageTokens each time; I saw the same opinion on stackOverflow where a guy suggested that youtube has actually never changed these tokens since not later than 2014. Thus I just listed those tokens in two array (check lines 67 - 69) and simply have used those arrays to itterate through while assembling a new url and fetch a new one each time a corresponding button is pushed.

I've restricted with 5 pages, each page renders 25 results (&maxResults=25) - if you want, you can add more tokens to iterate through/ more pages to be displayed.

Important note! These tokens are valid ONLY if displayed results per page are equal to 25 (&maxResults=25! I have noticed that if you change &maxResults = to any other value (say, 5 or 15), tokens will be different.
So should you want to have another number of results displayed - do not forget to adjust your arrays accordingly.

Thx 4 attention!
