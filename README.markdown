Gives you a `[name]_attributes=` setter method to create nested objects via params.

Example
-------

*contact.rb*

    builds_on :emails, :field_to_be_skipped_if_blank => "address"

*contacts/_form.html.erb*

    <%= text_field_tag "contact[email_attributes][][address]" %>

Options
-------

* `name` - Name of association in singular form.  I.E. address, email, etc.
* `field_to_be_skipped_if_blank` - If field is left blank, it will remove it from the
attributes before inserting.
* `destroy_associations` - Will destroy all existing associated objects before insert.
