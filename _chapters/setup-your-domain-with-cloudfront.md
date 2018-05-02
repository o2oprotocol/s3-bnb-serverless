---
layout: post
title: Set up Your Domain with CloudFront
date: 2017-12-09 00:00:00
description: To host our React.js app under our own domain name in AWS we are going to purchase a domain using Route 53. We will point the domain to our CloudFront Distribution with an Alias Resource Record Set. We also need to create an AAAA Record Set to support IPv6.
context: all
comments_id: 65
---

Now that we have our CloudFront distribution live, let's set up our domain with it. You can purchase a domain right from the [AWS Console](https://console.aws.amazon.com) by heading to the Route 53 section in the list of services.

![Select Route 53 service screenshot]({{ site.baseurl }}/assets/deploy-frontend/select-route-53-service.png)

### Purchase a Domain with Route 53

Type in your domain in the **Register domain** section and click **Check**.

![Search available domain screenshot]({{ site.baseurl }}/assets/deploy-frontend/search-available-domain.png)

After checking its availability, click **Add to cart**.

![Add domain to cart screenshot]({{ site.baseurl }}/assets/deploy-frontend/add-domain-to-cart.png)

And hit **Continue** at the bottom of the page.

![Continue to contact details screenshot]({{ site.baseurl }}/assets/deploy-frontend/continue-to-contact-details.png)

Fill in your contact details and hit **Continue** once again.

![Continue to confirm details screenshot]({{ site.baseurl }}/assets/deploy-frontend/continue-to-confirm-details.png)

Finally, review your details and confirm the purchase by hitting **Complete Purchase**.

![Confirm domain purchase screenshot]({{ site.baseurl }}/assets/deploy-frontend/confirm-domain-purchase.png)

Next, we'll add an alternate domain name for our CloudFront Distribution.

### Add Alternate Domain for CloudFront Distribution

Head over to the details of your CloudFront Distribution and hit **Edit**.

![Edit CloudFront Distribution screenshot]({{ site.baseurl }}/assets/deploy-frontend/edit-cloudfront-distribution.png)

And type in your new domain name in the **Alternate Domain Names (CNAMEs)** field.

![Set alternate domain name screenshot]({{ site.baseurl }}/assets/deploy-frontend/set-alternate-domain-name.png)

Scroll down and hit **Yes, Edit** to save the changes.

![Yes edit CloudFront changes screenshot]({{ site.baseurl }}/assets/deploy-frontend/yes-edit-cloudfront-changes.png)

Next, let's point our domain to the CloudFront Distribution.

### Point Domain to CloudFront Distribution

Head back into Route 53 and hit the **Hosted Zones** button. If you don't have an existing **Hosted Zone**, you'll need to create one by adding the **Domain Name** and selecting **Public Hosted Zone** as the **Type**.

![Select Route 53 hosted zones screenshot]({{ site.baseurl }}/assets/deploy-frontend/select-route-53-hosted-zones.png)

Select your domain from the list and hit **Create Record Set** in the details screen.

![Select create record set screenshot]({{ site.baseurl }}/assets/deploy-frontend/select-create-record-set.png)

Leave the **Name** field empty since we are going to point our bare domain (without the www.) to our CloudFront Distribution.

![Leave name field empty screenshot]({{ site.baseurl }}/assets/deploy-frontend/leave-name-field-empty.png)

And select **Alias** as **Yes** since we are going to simply point this to our CloudFront domain.

![Set Alias to yes screenshot]({{ site.baseurl }}/assets/deploy-frontend/set-alias-to-yes.png)

In the **Alias Target** dropdown, select your CloudFront Distribution.

![Select your CloudFront Distribution screenshot]({{ site.baseurl }}/assets/deploy-frontend/select-your-cloudfront-distribution.png)

Finally, hit **Create** to add your new record set.

![Select create to add record set screenshot]({{ site.baseurl }}/assets/deploy-frontend/select-create-to-add-record-set.png)

### Add IPv6 Support

CloudFront Distributions have IPv6 enabled by default and this means that we need to create an AAAA record as well. It is set up exactly the same way as the Alias record.

Create a new Record Set with the exact settings as before, except make sure to pick **AAAA - IPv6 address** as the **Type**.

![Select AAAA IPv6 record set screenshot]({{ site.baseurl }}/assets/deploy-frontend/select-create-aaaa-ipv6-record-set.png)

And hit **Create** to add your AAAA record set.

It can take around an hour to update the DNS records but once it's done, you should be able to access your app through your domain.

![App live on new domain screenshot]({{ site.baseurl }}/assets/deploy-frontend/app-live-on-new-domain.png)

Next up, we'll take a quick look at ensuring that our www. domain also directs to our app.
