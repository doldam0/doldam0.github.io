---
layout: page
title: Contact
permalink: /contact
comments: false
---

<form action="https://formspree.io/{{site.email}}" method="POST">    
<p class="mb-4">{{site.name}}에 메시지를 보내주세요. 곧 답장해 드립니다!</p>
<div class="form-group row">
<div class="col-md-6">
<input class="form-control" type="text" name="name" placeholder="이름*" required>
</div>
<div class="col-md-6">
<input class="form-control" type="email" name="_replyto" placeholder="이메일*" required>
</div>
</div>
<textarea rows="8" class="form-control mb-3" name="message" placeholder="메시지*" required></textarea>    
<input class="btn btn-dark" type="submit" value="보내기">
</form>