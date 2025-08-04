# GuestUser

- Description: guest user is anyone who visits the website to explore the rooms available for renting in the pg, or for any other purpose of his/her interest.
- Flow of available actions:
  Guest has access to 3 pages: Home, Rooms and Amenities
  -- Home: landing page, gives overview about the PG, reasons why you should chose this PG, etc.
  -- Rooms: shows available room types (Single room, double sharing, triple sharing) and has explore option for each room type
  [] on clicking explore s/he will see all the available rooms of that type: a page with cards having photo of the room and and other details with a book now option
  [] on clicking book now: the user would be directed to registration page, where s/he will see the room details in brief, will have to verify the email id, enter details - full name, contact number, gender, password, expected move in date, agreement to terms and conditions and then pay and confirm booking button
  [] on clicking pay and confirm booking page the user will see a popup or be redirect to a payment gateway (a third party app)
  [] once the payment is successful the user is redirected to a confirmation page and would receive an email with the confirmation

# Tenant

- Description: guest when books a room becomes a tenant from the day s/he moves in to the PG till s/he moves out
- Flow of available actions:
  Tenant has access to following pages: dashboard, payments/rent payment, notices, complaints, leavePG

  [] Dashboard : overview of some basic info

  - Greeting with tenant name, room number, and some other details like floor number
  - this page shows rent status of the current month (with next payment due date (calculated based on move-in date))
  - number of active complaints raised by the tenant
  - duration of tenancy in terms of months (from the day moved in)
  - list of 3-4 most recent activities: recent rent payment, recent leave request raised, complaints raised

  [] Payment : shows rent details, rent breakdown (monthly rent, maintenance charge, electricity charge, additional charge, additional service charges), pay button (which will redirect to third party payment gateway). This page would show only confirmation message if the rent for the current month is already paid and show the due date for next payment

  [] Notice Board: This page will display all the notices with tags - urgent, important, general, new (if the notice is less than 2 days old), with option to filter the notices based on these are tags

  [] Complaints: provides option to raise complaint and track previously raised

  - Raise complaints form on the top of the page : this has fields like - title, priority level, message, and raise complaints button
  - The form is followed by the cards of complaints raised earlier, with details - title, details of the issue, date raised, status of complaint (pending, resolved, in progress -- based on admin action), priority of the complaint, option to delete pending complaints

  [] Leave PG: through this page a tenant would be able to notify the admin about her/his intention/notice to leave the PG on intended and thus ask admin to start the settlement process

  - shows current tenancy details: room number, rent status, next payment due date
  - followed by notice details form: contains fields- intended move out date, reason for leaving, additional details, confirmation and acknowledgement of the PG rules/guidelines and the button to submit the notice
  - If the tenant has already submitted the leave notice then he will see the status of his settlement claim to security deposit (details of which would be discussed in the admin section)

# Admin

- Description: An user of the application delegated by the owner (or could be owner of the PG itself), is able to administrative work and get statistics through this section.
- Flow of available actions:
  Admin has access to following pages: Dashboard, rooms, tenants, notices, complaints, leave notices

  [] Dashboard: gives admin an overview of the important stats like total tenants, available occupancy, active complaints, Earning/ Revenue trend, occupancy rate, recent activities- around 4 most recent activities on the platform -- if tenant raise leave notice, complaint, someone paid rent, etc

  [] Rooms: page deals with activities and info related to rooms

  - has option(button) at the top to add new room which opens to form which has fields: room number, room size, room type, max occupancy, floor, monthly rent, facilities, upload photos of the room etc.
  - this page also list all the rooms, there basic details -- type, floor, rent, vacant, occupied status, facilities and option to hide or edit the rooms
    -- Am I missing any important things to add here?

  [] Tenants: refer https://pg-management-frontend-c4ae.vercel.app/admin/notices
  [] Notices: refer https://pg-management-frontend-c4ae.vercel.app/admin/notices
  [] Complaints: refer https://pg-management-frontend-c4ae.vercel.app/admin/complaints
  [] Leave Notices: refer https://pg-management-frontend-c4ae.vercel.app/admin/leave-notices
