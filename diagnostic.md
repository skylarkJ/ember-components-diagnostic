# Ember Components Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  Give an example of a visual hierarchy that could be modeled with components. Explain why each piece might be it's own component.

    ```md
  Sport Highlights - user 1: soccer (favorites: team 1, team 3), user 2: soccer(favorites: team 2, team 4, team 5)

  Type of sport like soccer, hockey, etc could be own component
    ```

1.  What is the command to generate a new component called '`my-map`'?

    ```sh
  ember generate component my-map
    ```

1.  What files are created and/or edited to produce a component, and what are their responsibilities?

    ```md
    create app/components/my-map.js
    create app/templates/components/my-map.hbs
    installing component-test
    create tests/integration/components/my-map-test.js
    ```

1.  Suppose you have a component '`my-contact`', which is loaded from
    '`app/contacts/template.hbs`' when visiting the `/contacts` route. What is
    the syntax (code that is written) to render this component inside that template?

    ```html
    import Ember from 'ember';

   export default Ember.Route.extend({
     model () {
       return [
         {
           name: 'Peter',
           phone: 5655444
         }, {
           name: 'Oliver',
           phone: 5555444
         },
       ];
     },
   });
    ```

1.  Each contact has multiple phone numbers. Suppose you also have '`my-phone`'
    nested under '`my-contact`'. What is the code you would write in
    '`app/components/my-contact/template.hbs`' to load the nested component and
    pass it data?

    ```html
    import Ember from 'ember';

   export default Ember.Route.extend({
     model () {
       return [
         {
           my-contact: 'Peter',
            my-phone: [
             {number1: 5655444,}
             {number2: 534434334,}
            ]
         }, {
           my-contact: 'Peter',
            my-phone: [
             {number1: 5655444,}
             {number2: 534434334,}
            ]
       ];
     },
   });
    ```
