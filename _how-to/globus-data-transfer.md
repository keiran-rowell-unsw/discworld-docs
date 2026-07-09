---
title: "Transfer data with Globus 🌐"
author: keiran_rowell 
globus_share_steps: 
    - image_path: /assets/images/globus-permissions-01.png
      alt: "Globus 'Permissions' management button"
      title: "Step 1"
    - image_path: /assets/images/globus-add-permissions-share-with-02.png
      alt: "Globus 'Add Permissions' sub-button"
      title: "Step 2"
    - image_path: /assets/images/globus-share-path-03.png
      alt: "Globus 'Path' to share a collection with a guest"
      title: "Step 3"
    - image_path: /assets/images/globus-share-email-04.png
      alt: "Globus 'Guest' share email address of proper name"
      title: "Step 4"
    - image_path: /assets/images/globus-email-message-05.png
      alt: "Globus email message to guest collaborator"
      title: "Step 5"
    - image_path: /assets/images/globus-rw-permissions-06.png
      alt: "Globus Read/Write permissions"
      title: "Step 6"
---



**Globus**  🌐📁🔀📁🌐<br>
Globus is the modern, secure, web interface to transfer between between research `endpoints`.
It _excels_ at transferring huge data sets across the network, and it's the preferred method to bring voluminous datasets onto Discworld 
{: .notice--info}

### Authentication 

🔑🦁 Globus handles data access securely with your university credentials.<br> 
Go to [app.globus.org](app.globus.org) and validate through your university (UNSW sign-on)
{: .notice--warning}

![Globus sign-on screen]({{ site.url }}{{ site.baseurl }}/assets/images/globus-app-unsw-sign-on.png)

Everything from here on in will engage your uni identity (`zID`)

![zID AD email Globus account]({{ site.url }}{{ site.baseurl }}/assets/images/zID_AD-identity.png)

The crown ♕ should be next to your UNSW provided identity:<br> **this is what you share with collaborators to enable data access**. 

### 📬 Sharing Files & Folders

Within the Globus `File Manager` you can share a Globus `collection` with another user through the `Permissions` system.

<div class="guide-marquee">
  <div class="marquee-item">
    <img src="/assets/images/globus-permissions-01.png" alt="Globus Permissions button">
    <p><strong>Step 1</strong></p>
  </div>
  <div class="marquee-item">
    <img src="/assets/images/globus-add-permissions-share-with-02.png" alt="Globus Add Permissions">
    <p><strong>Step 2</strong></p>
  </div>
  <div class="marquee-item">
    <img src="/assets/images/globus-share-path-03.png" alt="Globus Path to share">
    <p><strong>Step 3</strong></p>
  </div>
  <div class="marquee-item">
    <img src="/assets/images/globus-share-email-04.png" alt="Globus Guest share email">
    <p><strong>Step 4</strong></p>
  </div>
  <div class="marquee-item">
    <img src="/assets/images/globus-email-message-05.png" alt="Globus email message">
    <p><strong>Step 5</strong></p>
  </div>
  <div class="marquee-item">
    <img src="/assets/images/globus-rw-permissions-06.png" alt="Globus Read/Write permissions">
    <p><strong>Step 6</strong></p>
  </div>
</div>

<style>
  .guide-marquee {
    display: flex;
    overflow-x: auto;
    gap: 20px;
    padding: 15px 0;
    scroll-snap-type: x mandatory;
    -webkit-overflow-scrolling: touch;
  }
  .marquee-item {
    flex: 0 0 400px; /* Controls the width of each step card */
    scroll-snap-align: start;
    text-align: center;
    border: 1px solid #f2f3f3;
    padding: 10px;
    border-radius: 4px;
  }
  .marquee-item img {
    width: 100%;
    height: auto;
    display: block;
    margin-bottom: 10px;
    border-radius: 2px;
  }
</style>

### 📁 File Management

🔎 Most Globus data is in publicly searchable `collections`, but their contents are locked 🔒
{: .notice--info}


!["Sherlock" search ion Globus collections]({{ site.url }}{{ site.baseurl }}/assets/images/sherlock-collections.png)

You can contact your counterpart to request they to share a particular `collection` with your Globus identity
{: .notice--info}


### Definitions
Globus has [two core concepts](https://docs.globus.org/guides/overviews/collections-and-endpoints/): the Globus `endpoints` (organisational data transfer clearing house) and the `collections` (managed datasets) within them.

The nice thing is Globus `endpoints` are public ---searchable through the `📁 File Manager`--- while `collections` are private by default and you choose to share them with other uni indetities. 

#### `endpoints`

This is a specific location & server that manages the high-throughput data transfer work. It is set up by an organisational storage admin, so the the physical server gateway is configured for best data transfer & org policies.

The endpoint does the invisible mapping work so you can find the `collection` you are looking for.


#### `collections`

The collection contains raw datafrom which you can set off a `Transfer` job


#### `guest collections`

You can [Share Data Using Globus](https://docs.globus.org/guides/tutorials/manage-files/share-files/) without needing to touch the accounts on the underlying server.

You do this by creating a guest collection _within_ the `endpoint` your data is stored in. This is a `guest collection` that only sees your own data, and allows you to grant `Roles` to other Globus identities.

Please follow the 8 steps in [How To Share Data Using Globus](https://docs.globus.org/guides/tutorials/manage-files/share-files/) to manage your own `guest collection` and share an email invite. 
{: .notice--info}


### Discworld Globus details

#### University storage data mover 
Dedicated data mover servers exist to transfer your data onto the university central research storage solution (the `ESS`).
{: .notice--info}

While capacity is being added, transfers may be limited by total data pipeline until dedicated physical networking is configured. 

#### UNSW-EMU
A dedicated mapped `collection` exists that maps to `/data/lab/<lab_name>` to manage a lab group's data and interface with the `cryotem` instrumentation 
{: .notice--info}
```
Subscribed Mapped Collection (GCS) on ResTech (gd1) 
Owner: 9d5f4d54-e4b6-4834-9122-a4bef7ef7732@clients.auth.globus.org 
Domain: m-ff62ba.88a567.36fe.gaccess.io  
Description: (not set)  
Organization: The University of New South Wales (UNSW) 
Department: EMU
Subscription: University of New South Wales
Keywords: (not set) 
``` 

#### Discworld StructBio /User Data
A dedicated `collection` exists that maps to `/data/ess/<zID>` to cleanly structral data transfer from _external_ sources to UNSW `zID@ad.unsw.edu.au` email address.
{: .notice--info}
```
Subscribed Mapped Collection (GCS) on ResTech (gd1) 
Owner: 9d5f4d54-e4b6-4834-9122-a4bef7ef7732@clients.auth.globus.org 
Domain: m-XXXXXX.88a567.36fe.gaccess.io 
Description: External Structural Biology data (crystallography, cryo, beamline, etc) endpoint for UNSW researchers 
Organization: UNSW Mark Wainwright Analytical Centre  
Department: Structural Biology Facility 
Subscription: University of New South Wales
Keywords: Discworld, MWAC, structural-biology, cryoEM, crystallography 
``` 


### Assistance --- Data Sharing
Almost all collections you share will be `guest collections` within an existing `mapped collection`.<br><br>
Please [contact us](mailto:sbf+discworld@unsw.edu.au) if you'd like to access data not already in an existing collection
{: .notice--warning}
