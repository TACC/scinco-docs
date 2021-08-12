=====================
Administration Portal
=====================

SCINCO JupyterHubs include an administrative portal. This interface allows Hub administrators
to perform tasks such as:

* Starting and stopping servers on behalf of users
* Adding volume mounts to a Hub
* Adding custom images to a Hub

If you are a PI and would like to control administrative functions on your SCINCO JupyterHub,
please file a ticket for TACC staff to add you as an administrator.


Accessing the Administration Portal
===================================

TACC staff can add a user to the Administration Portal instance that is running in Kubernetes.
Typically, Administration Portals are available at ``https://<portal_name>-admin.io.jupyter.tacc.cloud``.
You will be prompted for your TACC username and password. If you have been granted access to
the Administration Portal, you can log in and make alterations to the JupyterHub


.. note::
    **TACC staff only**
    
    To add a user, you must log in to the Kubernetes namespace where the Administration
    Portal is running Type ``kubectl get pods`` to see running pods. You will see a list of pods that may look like this::

      NAME                          READY   STATUS    RESTARTS   AGE
      jhub-7d9dd7887b-qld5q         1/1     Running   0          46d
      jhub-admin-556866b6b8-p7r6v   1/1     Running   0          36d

    You can start a shell on the admin pod with the command ``kubectl exec --stdin --tty jhub-admin-556866b6b8-p7r6v -- /bin/bash``.
    Once you have a shell, run the following command ``python manage.py add_admin <username>``. The user
    will now be able to log in to the admin portal.


Using the Administration Portal
===============================

Once you have successfully logged in, you will see the main page:

.. image:: img/admin-portal-main.png

From here, you may choose the following options:

* :doc:`./hubadmin`
* :doc:`./mounts`
* :doc:`./images`
* :doc:`./usergroups`

.. warning::
   The JupyterHub must be restarted by TACC staff before any configuration changes will appear.