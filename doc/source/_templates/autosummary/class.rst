:orphan:

{{ objname | escape | underline }}

.. currentmodule:: {{ module }}

.. autoclass:: {{ objname }}

   {% block methods %}
   {% if methods %}
   .. rubric:: Methods

   {% for item in methods %}
   .. automethod:: {{ module }}.{{ objname }}.{{ item }}
      :no-index:
   {%- endfor %}
   {% endif %}
   {% endblock methods %}

   {% block attributes %}
   {% if attributes %}
   .. rubric:: Attributes
   
   {% for item in attributes %}
   .. autoattribute:: {{ module }}.{{ objname }}.{{ item }}
      :no-index:
   {%- endfor %}
   {% endif %}
   {% endblock attributes %}