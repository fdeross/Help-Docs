
<br>
<section class="index-list">
  <h4>ON THIS PAGE</h4>

- [Before you begin](#before-you-begin)
- [Service Fee](#service-fee)
- [Stripe transaction fee](#stripe-transaction-fee)
- [Example](#example)

</section>
<br>  

## Before you begin

There are several parts that make up fees on Frosting and Stripe.

- **Cost of Products**: This is the base cost that a baker sets when creating an item.  It could be increased by Variations or quantity or it could be decreased by a sale price or Promotion.
- **Promotion**: If you create a promo code and the customer uses it, this will decrease the price of the order or item.
- **Shipping**: Pickups are free for customers but you might have other shipping costs for Local Delivery or mail shipping.
- **Tax**: If your jurisdiction charges sales tax you will add this to your order.
- **Order Total**: Product, shipping, and sales taxes.
- **Charged Amount**: Order total plus Frosting's Service fee.  This is the amount passed to Stripe.
- **Payout**: This is the amount that Stripe will deposit into your account.

## Service Fee

Let's break down how we come up with the Service Fee.

#### Order Total

Order Total = ((Cost of Products - Promotion) + Shipping) + Tax

#### Charged Amount

Customers pay a service fee for using Frosting.  This service fee ranges from 9 - 13% of the Total Price.

Charged Amount = Order Total + Service Fee

#### Bakery Commission

We want to help as many small business owners as we can so we are waving the commission till June 2021.  Normally bakery's get a 95% commission.

## Stripe transaction fee

Payout = (Charged Amount - 2.9%) - .30

## Example

This looks complicated, so let's take an example.

Let's say your bakery is here in Bentonville and you sell a cake for $25.  The customer wants local delivery which you charge $5 for. To further complicate things you are giving 10% off for your top customers.

Cost of Products: $25
Promotion: -10%
Tax Rate: 9.5%
Shipping: $5
Service Fee: 9%

Cost of Products - Promotion = A
$25 - 10% [$2.50] = $22.50

A + Shipping = B
$22.50 + $5 = $27.50

B + Tax = Order Total
$27.50 + 9.5% [$2.61] = $30.11

Order Total + Service Fee = Charged Amount
$30.11 + 9% [$2.71] = $32.82

Order Total = $30.11

Charged Amount = $32.82

##### Now to Stripe and the Payout

$32.82 - 2.9% 

($25 - 2.9% [.73]) 

$24.27 - .30 = $23.97

The bakery's payout would be $23.97
