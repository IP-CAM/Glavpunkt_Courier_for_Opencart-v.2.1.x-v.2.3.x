# glavpunkt_courier_for_opencart-v.2.1.x-and-v.2.3.x-ocmod
The pick-up delivery service display template is located under the path 
public_html => catalog => view => theme => default => template => checkout => simplecheckout_shipping.tpl

JS code is inserted into html, via php, as a result, the "<" symbol was replaced by "<", in model glavpunkt.php, 
input validation in the field is added, administration => add-ons => delivery => free shipping => "Code JavaScript to change the rate ".
$ value) {if (isset ($ value ['description'])) {
$ order = array ("", "<", ">", "&", "" "," '"); $ replace = array ("", "<", ">", '"'," '"); 
$ newstr = str_replace ($ order, $ replace, $ value ['description']); $ shipping_method ['quote'] [$ key] ['description'] = $ newstr; }}}?>

The file public_html => catalog => model => extension => shipping => glavpunkt.php stores the model class, 
in which the value of the code entered by the user (in the module settings) is passed, to $ quote_data ['glavpunkt'] 
and $ method_data, then the output occurs in template (shipping_method.tpl)

description of modifiers in OpenCart https://opencart2x.ru/blog/vqmod-to-ocmod
Releases

Each version has its own releases. All releases are presented here - 
https://github.com/glavpunkt/OpenCartModules/releases. 
Versions have the following designations - v1.0.0a, where 1.0.0 is the module version, a (b, c, d) is the designation of the OpenCard version for 
which it is intended. a - 1.5, b - 2.1, c - 2.3, d - 3.0. When creating a new release, you must fill in the Tag version and Release Title fields, 
and be sure to check the correct Target. 
