---
layout: page
title: "Extending the User Model"
category: tut
date: 2014-11-20 15:06:34
order: 10
---

You can add methods to the user model by adding handlers. Your handler will have access to the User model in ```$this->user``` 

```
use Conductor\Core\UserHandler;

class PaymentHandler extends UserHandler {

  public pay($amount)
  {
      $paymentProvider->pay($amount, $this->user); 
  }

}
```
<br /><br />
The methods in your handler will be added to the user class.

```
$user = $user->find(1);

$user->pay(2500);
```