# ERPNext-DATEV_connector

As a result from the ERPNext Event in Wiesbaden, Germany on Nov. 21, 2018 this repositorie's goal is
to develop of a connector or adaptor to exchange accounting data between ERPNext and the DATEV.

DATEV is almost is holding a de facto monlopy in the German market for tax consultancies (Steuerberater) so 
ERPNext users in the Germany may be obligded to provide their accounting data to external consultants
or tax authorities in a format readable by DATEV.

The principles of this work to may apply to other external accounting systems as well though.

I personally am not a developer but aim to get the right group of people together and steer the project 
where needed.

It is still to be decided where in the end the best location of this repository is, but to get things started 
I have put it in my personal github for the time being.

---

I'd like to raise a technical and maintainance question about how a connector like this would work. 

I could imagine 3 scenarios

1. external independent Application, which (presumingly) would have to talk to ERPNext/Frappe's API
2. An external frappe App *2)
3. part of the ERPNext core *1)

   *1) I have learned from Charles (who also delivered a talk at the infamous Wiesbaden event) in the meantime that there is a Core Modul of ERPNext named [regional](https://github.com/frappe/erpnext/tree/develop/erpnext/regional) which can hold only regionally relevant code which than only gets installed if the company being setup is inside the relevant region. Currently there is some specific stuff for i.e. France & India (also accounting related I believe).

So, if technically doable (which others are more likely to be able to judge upon) this may be a slick option for housing our little connector here. The pro's are obvious. Once created it'll be maintained together with the core.

*2) has definitely the disadvantage of not being available to users of the cloud erpnext.com service unless someone would be able to make frappe pvt. treat it similar to the [Shopify Connector](https://github.com/frappe/erpnext_shopify)
