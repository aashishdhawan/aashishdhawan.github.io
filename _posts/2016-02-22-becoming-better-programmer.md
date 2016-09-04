---
title:  "Becoming a Better Programmer"
date:   2016-02-22 11:11:11
---

I stumbled upon this book [**Becoming a Better Programmer**](http://www.amazon.in/Becoming-Better-Programmer-Pete-Goodliffe/dp/1491905530)  couple of years back and liked it very much. Today i finished reading this book again. Well..Some books are meant to be read again and again. I would like to recommend this book to every beginner and even experienced developers can learn few things from it.

Here i am trying to create summary of this book in a hope to inspire you to read this book. Also my intention is to use this as notes in future.

* To write good code, you have to care about it. To become a better programmer you must invest time and effort.
* There is nothing wrong with an emotional response to code. Being proud of your great work, or disgusted at bad code, is healthy.
* Good code presentation reveals your code’s intent. It is not an artistic endeavour.
* We need good presentation to avoid making code errors. Not so we can create pretty ASCII art.
* Remember who you’re writing code for: other people.
* Never alter presentation and behaviour at the same time. Make them separate version-controlled changes.
* Less code can mean more software.
* Express code clearly and succinctly. Avoid unnecessarily long- winded statements.
* Do not copy code sections. Factor them into a common function. Use parameters to express any differences.
* If you spot duplication, remove it.
* Make sure that every comment adds value to the code. The code itself says what and how. A comment should explain why—but only if it’s not already clear.
* Do not remove code by commenting it out. It confuses the read‐ er and gets in the way.
* Every day, leave your code a little better than it was. Remove redundancy and duplication as you find it.
* You can improve a system by adding new code. You can also improve a system by removing code.
* Code cleanup should always be made in separate commits to functional changes.
* It is safe to remove code that you might need in the future. You can always get it back from version control.
* Looking back at your older code will inform you about the improvement (or otherwise) in your coding skills.
* Your best route into code is to be led by someone who already knows the terrain. Don’t be afraid to ask for help!
* Healthy projects require a single checkout to obtain the whole codebase, and the code can be placed in any directory on your build machine. Do not rely on multiple checkout steps, or code in hardcoded locations.
* A healthy build runs in one step, with no manual intervention during the build process.
* Pick your battles. Consider carefully whether you should invest time and effort in “tidying up” bad code. It may be pragmatic to leave it alone right now.
* Follow the Boy Scout Rule. Whenever you touch some code leave it better than you found it.
* Make code changes slowly, and carefully. Make one change at a time.
* There is no need to apportion blame for “bad” code.
* Do not ignore possible errors in your code. Don’t put off handling errors until “later” (you won’t get around to it).
* Use exceptions well, with discipline. Understand your language’s idioms and requirements for effective exception use.
* Consider all potential code paths as you write your code. Do not plan to handle “unusual” cases later: you’ll forget and your code will be buggy.
* Avoid injecting bugs into your code by employing sound engineering practices. Don’t expect quickly hacked-out code to be of high quality.
* Assertions and logging (even the humble printf) are potent de‐ bugging tools. Use them often.
* Binary chop problem spaces to get results faster.
* Untested code is a breeding ground for bugs. Tests are your bleach.
* Learn how to use your debugger well. Then use it at the right times.
* Fix bugs as soon as you can. Don’t let them pile up until you’re stuck in a code cesspit.
* To improve our software development we need rapid feedback, to learn of problems as soon as they appear. Good testing strategies provide short feedback loops.
* Write tests as you write the code under test. Do not postpone test writing, or your tests will not be as effective.
* Encourage tests to be run early and often. Bake them into your build process.
* Good development tests do not replace thorough QA testing.
* Bad tests can be a liability. They can impede effective development.
* Maintain your test suite, and listen to it when it talks to you.
* Global variables and singleton objects are anathema to reliable testing. You can’t easily test a unit with hidden dependencies.
* Factoring your code to make it “testable” leads to better code design.
* Poor company structure and unhealthy development processes will be reflected by a poor software architecture.
* Maintain the quality of a software design. Bad design leads to further bad design.
* The health of the working relationships in your development team will feed directly into the software design. Unhealthy relationships and inflated egos lead to unhealthy software.
* Good design takes into account connection mechanisms and the number (and nature) of inter-component connections. The individual parts of a system should be able to stand alone. Tight coupling leads to untestable code.
* A lax and fuzzy architecture leads to individual code components that are badly written and don’t fit well together. It also leads to duplication of code and effort.
* The consequences of a bad architecture are not constrained within the code. They spill outside to affect people, teams, processes, and timescales.
* A clear architectural design leads to a consistent system. All decisions should be taken in the context of the architectural design.
* Clear architecture helps reduce duplication of functionality.
* Defer design decisions until you have to take them. Don’t make architectural decisions when you don’t know the requirements yet. Don’t guess.
* Design quality must be maintained. This can only happen when the developers are given responsibility and take it seriously.
* Having a good set of automated tests for your system allows you to make fundamental architectural changes with minimal risk. It gives you space to work in.
* Unit testing your code leads to better software designs, so de‐ sign for testability.
* Good project planning leads to superior designs. Allot sufficient time to create an architectural masterpiece—they don’t appear instantly.
* A programmer needs good taste and a sense of aesthetics to write exceptional code.
* Good software development is not cowboy coding, throwing down the first code you can think of. It is a deliberate, considered, accurate endeavour.
* Good programmers work with humility. They admit that they don’t know it all.
* Programming teams have a set of rules. These rules define what we do and how we do it. But they also describe a coding culture.
* Don’t rely on vague unwritten team “rules.” Make the implicit rules explicit, and take control of your coding culture.
* Simple code takes effort to design. It is not the same thing as overly simplistic code.
* Simple designs aim to prevent misuse. They may involve extra internal complexity in order to present a simpler API.
* Simple designs are as small as possible. And no smaller.
* Consistency leads to clarity.
* Apply bugfixes to the root cause, not where symptoms mani‐ fest. Sticking plaster symptom-fixes do not lead to simple code.
* Avoid implicit assumptions in your code.
* Only write as much code as is needed. Anything extra is complexity that will become a burden.
* Stop and think. Don’t write stupid code.
* Admit to your mistakes and bad coding decisions. Learn from them.
* Pay attention. Don’t write code without care.
* Have the courage to use your brain. Feel empowered to critique code and make decisions about how to improve it.
* You are the master of your software; it’s under your control. Do not let the code, or the processes around it, dictate how the code grows.
* To modify code you need courage and skill. Not recklessness.
* “Good code” is not somebody else’s problem. It is your responsibility. You have the power to make a change and to bring about an improvement.
* Often it is best to make a series of frequent, small, verifiable adjustments, rather than one large sweeping code change.
* Automated tests are an invaluable safety harness that build confidence in your code changes.
* Avoid copy-and-paste coding. Factor your logic into shared functions and common libraries, rather than suffer duplicated code (and duplicated bugs).
* Don’t copy code you find on the Web into your project without carefully inspecting it first.
* Code should be “shared” because it is useful to multiple clients, not because the developers want to create a nifty shared library.
* Don’t dismiss other people’s code. It may be better to use exist‐ ing libraries rather than write your own version.
* Store every file that comprises your software project under ver‐ sion control. But store as little as possible; do not include any unnecessary files.
* Check in changes little and often.
* Source code inhabits the VCS it is stored in. The more mature a project, the more deeply it relies on this habitat.
* It is wrong to view software development as a linear process.
* Beware of fostering an artificial separation between development and testing efforts.
* Unhealthy team interactions result in unhealthy code.
* Not creating a QA build thoughtfully and carefully shows a lack of respect to the testers.
* Never rush the creation of a build. You will make mistakes.
* Testing will only reveal problems that software developers add‐ ed to the system (by omission or commission). If they find a fault, it was your fault!
* Cultivate a healthy respect for the QA team. Enjoy working with them to craft excellent software.
* “Code freeze” is the period leading up to a release when no changes are anticipated.
* We slow down development work to carefully shepherd a code line to release, managing the final fixes and changes carefully.
* Branch or bust.
* It’s not unusual (or wrong) to ship software that you know could be better.
* During code freeze you will accrue technical debt. Monitor this, and be prepared to pay the debt off soon after the release ships.
* Aim for code that never “freezes,” but is permanently ready to release to production.
* Creating software releases requires discipline and planning. It is more than hitting “build” in a developer’s IDE.
* Always build your software in a fresh checkout, from scratch. Never reuse old parts of a software build.
* Make your build as simple as a single step that automates all parts of the process. Use a scripting language to do this.
* Deploy your builds on a CI server to ensure their health. Make formal releases from the same system.
* Never release software without testing the final artefacts.
* Do not defer the planning and construction of a software re‐ lease process until the last minute. Build it early, iterate through builds rapidly and frequently. Debug the build like you’d debug any other software.
* Be in a state of continual learning. Always look to learn some‐ thing new.
* Learn to enjoy learning.
* Our learning is often too narrowly focused. Consider a wider sphere of reference. Draw inspiration from many fields.
* Use as many sources as possible to improve the quality of your learning.
* Takes notes as you learn. Even if you throw them away.
* Purposefully manage your knowledge portfolio.
* Teach a topic to learn that topic well.
* Using what you just learned cements it in your memory. Try examples, answer questions, create pet projects.
* Expect to invest time and effort to grow your skill set. This is a worthwhile investment; it will repay itself.
* Do not make yourself “indispensable” by writing unreadable or unnecessary “clever” code.
* Honour software licenses.
* Ensure appropriate credit is given for work you reuse in your codebase.
* Good attitudes towards code are also good attitudes to other programmers.
* Do not write software that will make another person’s life worse. This is an abuse of power.
* Treat others as you would like them to treat you.
* A tired programmer is of no use to anyone. Do not overwork. Know your limits.
* Don’t become a one-trick pony. Position yourself to face new challenges, learn, and grow as a developer.
* Working with your programming language is a relationship you have to work at each day.
* Good programmers are good communicators. They talk, write, code, listen, and read well.
* Don’t expect to become a language master overnight, and don’t get frustrated whilst you work at it.
* Take care of yourself. Maintain good posture as you work.
* Use existing code, rather than writing your own from scratch. Employ your time on more important things.
* Concentrate effort on the most important things first. What is most urgent, or will produce the most value?
* Remember KISS: Keep It Simple, Stupid.
* If you do something often, make the computer do it for you. Automate it with a script.
* Make sure you define “done.”
* If you can’t tell when it’s done, then you shouldn’t start it.
* Use tests written in code to define when your code is complete and working.
* Don’t do more work than necessary. Work until you’re “done.” Then stop.
* Purposefully place yourself beside excellent programmers.
* More comments do not necessarily make your code better. Communicative code does not need extra commentary to prop it up.
* How well code communicates depends on the programming language, idioms employed, and the underlying natural language. All these have to be understood by the readership.
* Master the different forms of communication. Use the appropriate mechanism for each conversation.
* Take care to use the right vocabulary with the right people.
* Effective communication requires focus.
* Good communication fosters good code. The shape of your communications will shape your code.
* Speak to others transparently, with a healthy attitude, to foster effective teamwork.
* Learn about development methodologies, trends, manifestos, and fads.
* Subscribe to development manifestos that seem sensible. But don’t blindly follow them, and don’t treat them dogmatically.
* When surrounded by coders who do not care about the code, maintain healthy attitudes yourself. Beware of absorbing bad practices by osmosis.

Happy coding!!!
