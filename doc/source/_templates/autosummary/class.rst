:orphan:

{{ objname | escape | underline }}

.. currentmodule:: {{ module }}

.. autoclass:: {{ objname }}
   
   {% block methods %}
   {% if methods %}
   .. rubric:: Methods
   .. autosummary::
      :toctree: .
      {% for item in methods %}
      {{ objname }}.{{ item }}
      {%- endfor %}
   {% endif %}
   {% endblock %}

   {% block attributes %}
   {% if attributes %}
   .. rubric:: Attributes
   .. autosummary::
      :toctree: .
      {% for item in attributes %}
      {{ objname }}.{{ item }}
      {%- endfor %}
   {% endif %}
   {% endblock %}

   Method Details
   -------------
   
   .. automethod:: __init__
   
   {% block methods_details %}
   {% if methods %}
   {% for item in methods %}
   .. automethod:: {{ item }}
   {%- endfor %}
   {% endif %}
   {% endblock %}