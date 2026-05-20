Nathan Lin

1) Where would you fit your automated tests in your Recipe project development pipeline? Select one of the following and explain why.

    **Within a Github action that runs whenever code is pushed.**

    This would fit the automated tests in GitHub actions because the tests would run automtically upon certain events. Manually running the tests locally before pushing the code can introduce human error if the person pushing forgets to test, while GitHub actions can use a virtual machine to run the tests automatically after the person pushes. Running the tests after all development is completed is also a bad idea since by then, the program can be riddled with bugs.

2) Would you use an end to end test to check if a function is returning the correct output? (yes/no)

    **no**

    A better option might be to use Jest (i.e `expect(<function>).toBe(correct)`)

3) What is the difference between navigation and snapshot mode?
   
   Navigation mode reports on the performance on a fresh page reload, which is done by clearing the browser's cache to imitate a first time visitor. Snapshot mode reports on the current state of the web page at a single point in time.

4) Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.

    **Based on the lighthouse results, some nice improvements would be to**
   - Add a `[lang]` attribute to the `<html>` elements. Screen readers will currently assume that the page is in the user's default screen reader language which may result in a page's text being incorrectly announced.
   - Lighthouse says that `issues` were logged in Chrome Devtools. Specificially, it says "Content Security Policy of your site blocks the use of 'eval' in Javascript." This is a security feature blocking "injection sinks" from running which bars people from running unauthorized scripts.
   - Lighthouse says "Document does not have a meta description" which are included in search results to concisely summarize page content. The HTML can be formatted in a way that is easier for crawlers to read.


