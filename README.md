Nathan Lin

1) Where would you fit your automated tests in your Recipe project development pipeline? Select one of the following and explain why.

**Within a Github action that runs whenever code is pushed.**

This would fit the automated tests in GitHub actions because the tests would run automtically upon certain events. Manually running the tests locally before pushing the code can introduce human error if the person pushing forgets to test, while GitHub actions can use a virtual machine to run the tests automatically after the person pushes. Running the tests after all development is completed is also a bad idea since by then, the program can be riddled with bugs.

2) Would you use an end to end test to check if a function is returning the correct output? (yes/no)

**no**

A better option might be to use Jest (i.e `expect(<function>).toBe(correct)`)

3) Navigation mode reports on the performance on a fresh page reload, which is done by clearing the browser's cache to imitate a first time visitor. Snapshot mode reports on the current state of the web page at a single point in time.

4) Name three things we could do to improve the CSE 110 shop site based on the Lighthouse results.

**Based on the lighthouse results, some nice improvements would be to**
- Optimize viewport for mobile: Lighthouse reports that tap interactions may be delayed by up to 300 ms if the viewport is not optimized for mobile. Although that delay may sound minimal, it the user will likely feel the delay which affects the user experience on the website.
- There are many reports of unused/duplicate code (Duplicated JavaScript, Reduce unused CSS, Reduce unused JavaScript): So it can be a great idea to go through and clean out unused lines to reduce unnecessary bytes consumed by network activity.
- Accessibility (Buttons have an accessible name, Input buttons have discernible text): Lighthouse reports that some of the elements on the page, such as buttons but be unusable by users who rely on screen readers (The button's name/purpose is not clear). 


