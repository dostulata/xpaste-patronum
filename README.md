# xpaste-patronum
Educational suff for ansible studies

Prerequisites.

On control node running this play:
  - ansible-galaxy collection install community.general
  - ansible-galaxy role install geerlingguy.nginx

On victim machine:
  - vanilla centos7
  - running openssh-server
  - user 'johndoe' in group 'wheel' with password '54321' -- there was no time
  - code of xpaste_practicum in /root/xpaste_practicum cloned from you-know-where -- there was no time at all

Ofcourse, many things about this play and roles can be improved, but it does it's job.
Stuff to improve:
  - clone app from git automatically (ssh keys and other stuff)
  - hide credentians, despite of they are not of a big value
  - use vault for keys and passwords
  - remove hardcode (paths mostly), beautify vars (envs especially)
  - use modules instead of shell where they can be used
  - add checks for idempotency of shell usages here and there
