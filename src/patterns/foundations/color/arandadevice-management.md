---
title: Feedback
styles: base/variables.scss
maturity: draft
control: exclude
colors:
  - name: $aqua
    hex: '#00A1C6'
    rgb: rgb(0,161,198)
  - name: $aqua_low
    hex: '#99f5ff'
    rgb: rgb(153,245,255)
  - name: $blue_high
    hex: '#425966'
    rgb: rgb(66,89,102)

---
<style>
.set {
  display: flex;
  flex-wrap: wrap;
  margin: 0 -1rem;
  margin-top: 0;
  padding: 0;
  list-style: none;
}
li {
  flex: 1 0 20%;
  margin: 1rem;
}
.color {
  width: 100%;
  min-width: 160px;
  height: 80px;
  color: white;
  border: 1px solid whitesmoke;
  margin-bottom: 1rem;
}
p {
  margin: 0;
}
</style>
<ul class="set">
{% for item in page.colors %}
  <li>
    <div class="color" style="background:{{ item.hex }}"></div>
    <p>{{ item.name }}</p>
    {% if item.hex %}<p>{{ item.hex }}</p>{% endif %}
    {% if item.rgb %}<p>{{ item.rgb }}</p>{% endif %}
  </li>
{% endfor %}
</ul>
