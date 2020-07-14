---
title: "Creating a Code Challenge"
description: "Creating challenges that ask users to submit code to reaches a solution"
---

In order to create a challenge you must be an admin.

1. Go to the admin panel by clicking the Admin button on the top right.

2. Click on the Challenges tab

   ![](/images/challenges/create-button-icon.png)

3) Select the "code" challenge type from the dropdown menu

   ![](/images/challenges/dynamic-challenge-dropdown.png)

4) Enter the standard values for the challenge, the only different field you need to specify is the language that participants need to use.

   ![](/images/challenges/code-challenge-selections.png)

5) Go to the challenge page and create a code flag type.

   ![](/images/challenges/code-select-flag.png)

6) The stdin field refers to any values you want passed to the user code. The stdout field is what the correct output should be when passed that input.

   ![](/images/challenges/code-flag-options.png)

7) Now when the particpant submits the following code, CTFd will execute the code with the parameters and compare it to the set stdout.

   ![](/images/challenges/code-challenge-solution.png)
