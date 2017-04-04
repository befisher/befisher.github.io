# Positively Write CRUD for Small Apps

*I found it boring to write [CRUD(Create/Retrieve/Update/Delete)][wiki-crud] operations all the time and I hope this post may be helpful for you to write CRUD positively especially for small applications.*

<!-- > Created by Fisher at 15:04 on 2017-04-04. -->

## Tired to Write CRUD

Repeating CRUD all the time can be tedious since one's initiative and creativity is depressed and we are going to make it better.

## Creating a Universal Abstract Helper

Obeying the Do-Not-Repeat-Yourself principle, you may come into mind of creating a universal abstract helper and share it with others. Gradually, you will find them slightly different from each other. you have been creating several different Helpers for different purpose. In the end, however, it is likely that you will not want to work on the maintainability any more.

## Customized Authorization & Filter for User Input Make it more Complex

Generally, **Authorization** and **User Input Filter** will make your small app complex and narrow purposed.

**_Authorization_ and *User Input Filter* varies based on what you are doing.** User Input Filter is important even for small apps. Since you expect a positive number(less than 100 let us say) provided from user or just keep your database logically acceptable, **time** and *efforts* and **tests** and **patience** are needed to make your server work with less exceptions or crashes.

**As your app becoming bigger, *Authorization* will also change consequently.** You may want more user types, e.g., VIP, Administrator, Super-Administrator, User Relations(Collaborators/Membership). You can either write more API for these special users or add privileges filter for each API.

As a result, a lot of work is required to create a universal template.

## Positively Write CRUD

- **Simple CRUD**
	0. Write a `SimpleCRUDHelper` template with configuration supported.
	0. Create instances using the `SimpleCRUDHelper` with customized options.
- **Complex CRUD** for some core/complex services for your app.
	0. Write a template for the basic CRUD operations.
	0. Make a copy and customize it to fit your need.


## References

*Keeping an eye on what is going on in bigger communities will always help :)*

- [Github Developer][github-developer]
- [Github Developer Documentation][github-developer-documentation]
- [Wiki: Create Read Update Delete][wiki-crud].


[github-developer]: https://developer.github.com/ "Github Developer"
[github-developer-documentation]: https://developer.github.com/v3 "Github APIs Documentation"
[wiki-crud]: https://en.wikipedia.org/wiki/Create,_read,_update_and_delete "Wiki: Create Read Update Delete"
