# adorsys REST test template

Simple Template for testing your RESTful Resources.

## Usage

Edit the index.html and add a form  for each Resource. Example:

    <form id="peopleForm" action="/test/clients/{clientId}/people.json?order={order}" method="GET">
      <fieldset>

        <legend>Order</legend>

        <label for="clientId">Client ID</label>
        <input id="clientId" type="text" value="4711" />

        <label for="order">Order</label>
        <input id="order" type="text" value="asc" />

        <input id="people" type="submit" />

      </fieldset>
    </form>

### Conventions

* You need a form with a action, method and one input type=submit.
* Parenthesized parts of the action will be replaced by the values of input fields with a according id.
* Named input fields will be serialized as form-data, others not.
* If you want to pass HTTP-headers add a input-field with the according data-header attribute.

Happy Testing!
