# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components.

    ```md
    In the Listr App, the overall Listr (list of lists) was a componenet, as were the individual lists (e.g., Favorite Things).
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
    ember g component my-map
    ```

1.  What files are edited to produce a component, and what are their
    responsibilities?

    ```md
    As an example, for the item component:
    * app/components/listr-list/item/component.js
      * for tying the item component to certain behvaiors -> striking out item text on click
    * app/components/listr-list/item/template.hbs
      * for templating the html markup -> creating a bullet point list of items
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` path. What is
    the syntax for loading this component inside that template?

    ```html
    {{my-contact contact=model}}
    ```

    Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    {{my-contact/my-phone contact=contact}}
    ```
