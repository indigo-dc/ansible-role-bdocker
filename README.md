# ansible-role-bdocker
<p>Ansible Role to install bdocker in a cluster.</p>
<p>At this point in time, this role assumes that you are working with a Systemd enabled OSs.</p>
<p>So far it has been tested on CentOS 7.</p>
<p>bdocker repo: https://github.com/indigo-dc/bdocker</p>
<p>bdocker documentation: https://www.gitbook.com/book/jorgesece/bdocker/details</p>

## Inventory file sample:
<pre><code>
[ui]
cluster-ui

[frontend]
cluster

[wn]
cluster-wn[01:02]

[storage]
st
</code></pre>

## How to add this role to your playbook
<pre><code>
 - name: Install bdocker
   hosts: all
   become: yes
   roles:
   - { role: ansible-role-bdocker, tags: [ 'bdocker' ] }
</code></pre>

