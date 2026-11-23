---
title: "ਕਿਸੇ ਕਲਾਕਾਰ ਦੀ ਸਿਫ਼ਾਰਸ਼ ਕਰੋ"
slug: suggest-an-artist
---

ਮੈਨੂੰ ਯਿਸੂ ਦੀ ਪਾਲਣਾ ਕਰਨ ਵਾਲੇ ਸੰਗੀਤਕਾਰਾਂ ਅਤੇ ਕਲਾਕਾਰਾਂ ਬਾਰੇ ਸੁਣਨਾ ਬਹੁਤ ਪਸੰਦ ਹੈ। ਜੇ ਤੁਸੀਂ ਕਿਸੇ ਅਜਿਹੇ ਵਿਅਕਤੀ ਨੂੰ ਜਾਣਦੇ ਹੋ ਜਿਸ ਬਾਰੇ ਤੁਸੀਂ ਚਾਹੁੰਦੇ ਹੋ ਕਿ ਮੈਂ ਲਿਖਾਂ, ਉਸਦੀ ਇੰਟਰਵਿਊ ਲਵਾਂ ਜਾਂ ਉਸ ਬਾਰੇ ਪ੍ਰਤੀਕਿਰਿਆ ਵੀਡੀਓ ਬਣਾਵਾਂ, ਤਾਂ ਇੱਥੇ ਮੈਨੂੰ ਦੱਸੋ।

ਇੱਕ ਨਾਂ ਅਤੇ ਇੱਕ ਲਿੰਕ ਕਾਫ਼ੀ ਹੈ — ਅਤੇ ਕੁਝ ਸ਼ਬਦਾਂ ਵਿੱਚ ਕਿਉਂ ਉਹ ਵਿਅਕਤੀ। ਜੋ ਕੁਝ ਆਉਂਦਾ ਹੈ ਮੈਂ ਸਭ ਪੜ੍ਹਦਾ ਹਾਂ। ਬਹੁਤ ਬਹੁਤ ਧੰਨਵਾਦ।

ਕੀ ਤੁਸੀਂ ਕਿਸੇ ਨੂੰ ਜਾਣਦੇ ਹੋ? ਉਸਦੀ ਫ਼ੋਟੋ ਨੂੰ ਛੂਹੋ, ਫ਼ਾਰਮ ਆਪਣੇ ਆਪ ਭਰ ਜਾਵੇਗਾ — ਫਿਰ ਕੁਝ ਸ਼ਬਦਾਂ ਵਿੱਚ ਜੋੜੋ ਕਿ ਕਿਉਂ ਉਹ ਵਿਅਕਤੀ, ਅਤੇ ਭੇਜੋ।

<div class="suggest-carousel" role="list" aria-label="ਸੰਗੀਤਕਾਰ ਅਤੇ ਕਲਾਕਾਰ ਜਿਨ੍ਹਾਂ ਦੀ ਤੁਸੀਂ ਸਿਫ਼ਾਰਸ਼ ਕਰ ਸਕਦੇ ਹੋ">
{% for artist in suggest_carousel %}
  <button type="button" class="suggest-pick" role="listitem" data-artist="{{ artist.name }}" data-link="{{ artist.profile }}" title="{{ artist.name }} ਦੀ ਸਿਫ਼ਾਰਸ਼ ਕਰੋ">
    <img src="{{ artist.img }}" alt="{{ artist.name }}" loading="lazy" width="150" height="150">
    <span class="suggest-pick__name">{{ artist.name }}</span>
    <span class="suggest-pick__note">{{ artist.note }}</span>
  </button>
{% endfor %}
</div>

<p class="suggest-carousel__more">ਜਾਂ ਹੇਠਾਂ ਕਿਸੇ ਨਵੇਂ ਵਿਅਕਤੀ ਦੀ ਸਿਫ਼ਾਰਸ਼ ਕਰੋ — ਕੋਈ ਵੀ ਜਿਸ ਬਾਰੇ ਤੁਹਾਨੂੰ ਲੱਗਦਾ ਹੈ ਕਿ ਮੈਨੂੰ ਸੁਣਨਾ ਚਾਹੀਦਾ ਹੈ।</p>

ਇਹ ਸਾਈਟ 18 ਸਾਲ ਤੋਂ ਘੱਟ ਉਮਰ ਦੇ ਲੋਕਾਂ ਲਈ ਨਹੀਂ ਹੈ।

<form id="suggest-form" class="suggest-form">
  <label for="suggest-artist">ਕਲਾਕਾਰ ਦਾ ਨਾਂ</label>
  <input id="suggest-artist" name="artist" type="text" maxlength="200" placeholder="ਮੈਂ ਕਿਸ ਵੱਲ ਦੇਖਾਂ?" required>

  <label for="suggest-link">ਸੋਸ਼ਲ ਮੀਡੀਆ ਪ੍ਰੋਫ਼ਾਈਲ ਦਾ ਲਿੰਕ</label>
  <input id="suggest-link" name="link" type="url" maxlength="500" placeholder="https://www.instagram.com/…" required>

  <fieldset class="suggest-kinds">
    <legend>ਮੈਂ ਉਨ੍ਹਾਂ ਨਾਲ ਕੀ ਕਰਾਂ?</legend>
    <label><input type="checkbox" name="kind" value="write"> ਉਨ੍ਹਾਂ ਬਾਰੇ ਲਿਖੋ</label>
    <label><input type="checkbox" name="kind" value="interview"> ਉਨ੍ਹਾਂ ਦੀ ਇੰਟਰਵਿਊ ਲਓ</label>
    <label><input type="checkbox" name="kind" value="reaction"> ਉਨ੍ਹਾਂ ਬਾਰੇ ਪ੍ਰਤੀਕਿਰਿਆ ਵੀਡੀਓ ਬਣਾਓ</label>
  </fieldset>

  <label for="suggest-why">ਕਿਉਂ ਉਹ?</label>
  <textarea id="suggest-why" name="why" rows="3" maxlength="500" placeholder="ਕੁਝ ਸ਼ਬਦ ਕਾਫ਼ੀ ਹਨ…"></textarea>

  <label for="suggest-name">ਤੁਹਾਡਾ ਨਾਂ <span class="optional">(ਵਿਕਲਪਿਕ)</span></label>
  <input id="suggest-name" name="fromName" type="text" maxlength="100" placeholder="ਤਾਂ ਜੋ ਮੈਂ ਧੰਨਵਾਦ ਕਰ ਸਕਾਂ">

  <label for="suggest-from-link">ਤੁਹਾਡੇ ਸੋਸ਼ਲ ਮੀਡੀਆ ਪ੍ਰੋਫ਼ਾਈਲ ਦਾ ਲਿੰਕ <span class="optional">(ਵਿਕਲਪਿਕ)</span></label>
  <input id="suggest-from-link" name="fromLink" type="url" maxlength="500" placeholder="https://www.instagram.com/…">

  <button id="suggest-button" type="button">ਸਿਫ਼ਾਰਸ਼ ਭੇਜੋ</button>

  <p id="suggest-result" aria-live="polite"></p>
</form>
