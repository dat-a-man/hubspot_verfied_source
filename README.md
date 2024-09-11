# hubspot_verfied_source

This is a modified Hubspot verified source which is created based on [dlt-dbt-package](https://github.com/dlt-hub/dlt_dbt_hubspot/tree/main/hubspot).

What's different?
- As in the above package, there is a resource template but it depends on different prop settings in "settings.py".

- Then owners is removed from hubspot source as a @dlt.resource, but used as "yield dlt.resource" 

- The "include_custom_props" param was causing some issue for owners as it is not available for owners. So fixed it. 

- binding props to endpoints is still not working so need help on that 

This source loads the following resources.  Available resources are: {
 'quotes', 'quotes_property_history', 'products_property_history', 'tickets', 'companies_property_history', 'contacts', 'companies', 'owners_property_history', 'stages_timing_deals',
 'deals_property_history', 'tickets_property_history', 'deals', 'pipelines_deals', 'contacts_property_history', 'products', 'properties', 'owners'}