# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
    The Reddit homepage
    Navbar at the top has links to subreddits. Each of those is a component because they
    depend on the user logged in and will repeat for how many subreddits they like.
    Each post on the homepage (and subreddit homepages) is a card component that varies
    based on the post, the type of post, the user who created the post, etc.
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    component.js - manages actions and other properties like class name bindings
    template.hbs - renders the component
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    {{my-contact contact=contact}} <!-- the second part may vary based on variable names -->
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{my-contact/my-phone contact=contact}} <!-- the second part may vary based on variable names -->
    ```
