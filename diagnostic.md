# Ember Routing Diagnostic

Record your responses inside the fenced code blocks below each question.

1.  What are the main task(s) you perform inside the Ember Application Router,
    and what are the main task(s) you perform inside an Ember Route?

    ```md
    You define all of the views/urls in the router. The main tasks you perorm in an ember route is either defining the data, applying data hooks and defining actions
    ```

1.  What is the command to generate a route named `boston` nested under
    `campus`?

    ```md
    ember g route campus/boston
    ```

1.  Suppose you have a nested route at the URL `/campus/boston`. How would you
    use the `link-to` helper to generate an appropriate link?

    ```md
  {{#link-to 'campus.boston'}}Boston{{/link-to}}
    ```

1.  Explain **at least** two differences between the following two route
    definitions.

    ```js
    this.route('products', function () {
      this.route('product', { path: '/:product_id' }); // <= 👀here
    });

    this.route('product', { path: '/products/:product_id' }); // <= 👀 here
    ```

    ```md
    The second route is a 'nested route.' The first route would show a single product where as
    the second route would most likely show a list of products.
    ```

1.  Suppose we have the following route definition:

    ```js
    this.route('movie', { path: '/movies/:movie_id' }); // <= 👀 here
    ```

    If we navigate in the browser to `/movies/123`, how can we reference the
    value `'123'` inside a Route?

    ```md
    I dont really understand this one...the value of 123 is referenced inside that route.
    ```

1.  Inside a template, how do we reference data provided by a Route?

    ```md
    By first referencing the appropriate model and second assigning it to a variable most likely called the same thing. For example:

    {{#each model as |list|}}
        {{listr-list/card list=list}}
      {{/each}}

      We're defining the model as list and saying we want the listr-list/card data. Then assigning the left list the value of the right list.
    ```
