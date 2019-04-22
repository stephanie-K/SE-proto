# GOV.UK Prototype Kit · used unbranded for Scottish Enterprise

Original website is here: [Scottish Enterprise](https://www.scottish-enterprise.com/)

To learn about the [GOV.UK Prototype Kit](https://govuk-prototype-kit.herokuapp.com/docs). You can download the latest version and read the documentation.

## About the Prototype Kit

The Prototype Kit provides a simple way to make interactive prototypes that look like pages on GOV.UK. These prototypes can be used to show ideas to people you work with, and to do user research.

Read the [project principles](https://govuk-prototype-kit.herokuapp.com/docs/principles).

## Customising it for Scottish Enterprise
- change the **favicon** in the layout and add it to app>assets>images
- customise the **header** and the **footer** in the **layout** and create a special file for it: app>views>layout_se.html
- add **specific CSS** and link for it in layout_se.html: app>assets>sass>se.scss
- for the **breadcrumbs**, I modified the macro for the general template in node-modules>govuk-frontend>template.njk to be able to declare a block called "postHeader" to be generated just after the header. For more advanced behaviour I would need to change the existing macro for the breadcrumbs to add specific se classes in node-modules>govuk-frontend>components>breadcrumbs>template.njk 
- for the **change of template in govuk-frontend** to be taken into account, I need to change **gitignore** to push the changes in node_modules
- to be able to deploy to Heroku, I commented a line of code in:  node_nmodules>browser-sync>dist>index.js / it's password protected
