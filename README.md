# System-Configuration

Create Virtual Host in LAMP of UBUNTU

/opt/lampp/etc/extra/httpd-vhosts.conf

    <VirtualHost *:80>
    ServerAdmin projectName.local
    DocumentRoot "/opt/lampp/htdocs/Project-Name"
    ServerName projectName.local
    </VirtualHost>

---------------
 etc/hosts
 
 127.0.0.1	projectName.local
 
 --------------
 /opt/lampp/etc/httpd.conf      //line 487-488
 
   # Virtual hosts
   Include etc/extra/httpd-vhosts.conf
 =================================================================
 
 Create Virtual Host in Windows

D:\xampp\apache\conf\extra\httpd-vhosts.conf

    <VirtualHost *:80>
    DocumentRoot "D:\xampp/htdocs/Project-Name"
    ServerName Project-Name.local
    <Directory "D:\xampp/htdocs/Project-Name">
    </Directory>
    </VirtualHost>
    
----------------------------------------------

C:\Windows/System32/drivers/etc/hosts

127.0.0.1  Project-Name.local

=================================================================





























<form data-name="Email Form 2" data-block-field="form" data-type="entity_reference" data-form-type="entity_reference_autocomplete" data-format-type="entity_reference_entity_view" data-target-type="contact_form" data-target-bundle="contact_us" data-form="contact_us">
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">Questions or comments*</label>
              <p class="body-sm">* = Required field</p>
            </div>
            <div class="_75-pc w-clearfix">
              {{ content.contact_us_question }}</div>
          </div>
          <h3 class="secondary">Your Details</h3>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">First name*</label>
            </div>
            <div class="_75-pc">
              {{ content.contact_us_first }}</div>
          </div>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">Last name*</label>
            </div>
            <div class="_75-pc">
              {{ content.contact_us_last }}</div>
          </div>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">Email*</label>
            </div>
            <div class="_75-pc">
              {{ content.contact_us_email }}</div>
          </div>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">State*</label>
            </div>
            <div class="_75-pc w-clearfix">
              {{ content.contact_us_state }}</div>
          </div>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">Contact phone</label>
            </div>
            <div class="_75-pc">
              {{ content.contact_us_first }}</div>
          </div>
          <div class="extra-margin separator-line"></div>
          <h3 class="secondary">Products</h3>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">Which products are you contacting us about?</label>
            </div>
            <div class="_75-pc w-clearfix">
              {{ content.contact_us_product }}</div>
          </div>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">Product Lot Code</label>
            </div>
            <div class="_75-pc">
              {{ content.contact_us_code }}<a class="w-inline-block w-lightbox" href="#">
                <div>Where do I find the product lot code?</div>
                <script class="w-json" type="application/json">
                  { "items": [{
                    "_id": "578e74a27230cb134371da96",
                    "cdnUrl": "https://daks2k3a4ib2z.cloudfront.net/57926c00412fc21f2b642fc1/57926c00412fc21f2b6430c0_vintage2.jpg",
                    "fileName": "57926c00412fc21f2b6430c0_vintage2.jpg",
                    "origFileName": "vintage2.jpg",
                    "width": 670,
                    "height": 390,
                    "fileSize": 84978,
                    "type": "image",
                    "url": "images/vintage2.jpg"
                  }] }
                </script></a>
            </div>
          </div>
          <div class="extra-margin separator-line"></div>
          <h4 class="secondary">Sign up for more info</h4>
          <div class="w-checkbox w-clearfix">
            {{ content.contact_us_sign_up }}<label class="w-form-label" for="Sign-Up-For-Newsletter-3">
              I would you like to sign up for coupons, promotions, newsletters and specials from Imperial Sugar.
            </label>
          </div>
          <div class="extra-margin separator-line"></div>
          <h4 class="secondary">Help us improve this website</h4>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">I am a&hellip;</label>
            </div>
            <div class="_75-pc w-clearfix">
              {{ content.contact_us_role }}</div>
          </div>
          <div class="form-input-wrapper w-clearfix">
            <div class="_25-pc">
              <label for="Recipe-name">How did you hear about us?</label>
            </div>
            <div class="_75-pc w-clearfix">
              {{ content.contact_us_how }}</div>
          </div>
          <div class="extra-margin separator-line"></div>
          <div>
            <div class="txt-centered">
              <input class="btn btn-form btn-submit w-button" data-ix="modal-form-thanks-show" data-wait="Please wait..." type="submit" value="Send inquiry"></div>
          </div>
          </form>
