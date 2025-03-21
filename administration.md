# Various admin notes 

# If VM is not sending log data and is behind load balancer, try this
  - Go to VM
  - Networking
  - NIC
  - IP configurations
  - Add IP address
  - Create new
    - vm-pip
    - standard sku
    - save
    - refresh

# How to activate GA through PIM process
  - As user
  - Go to entra ID
  - Roles and Administrators (Your role)
  - Choose Global Admin
  - Eligible assignmnets
  - activate (choose time)
  - wait

# Add external user to your Azure env
  - Users
  - new users
  - invite external user
  - check and see if user is in list
  - add email account
  - send link to user with tenant ID to portal url (ie: portal.azure.microsoft.cloud)
  - They must accept the license agreement
  - add use to appropiate groups
