---
layout: ContentPage
page_type: profile
page_kind: register
title: Register | Technical Profile
description: Register technical profile
---
<div id="register-container" class="container">
    <div id="register" class="columns is-hidden has-margin-none has-padding-top-extra-large-tablet is-centered">
        <div id="register-panel" class="column is-half-desktop is-10-tablet has-padding-none-mobile">
            <form id="register-form" class="card has-padding-top-extra-large-tablet has-padding-bottom-extra-large-tablet has-padding-left-extra-large-tablet has-padding-right-extra-large-tablet has-padding-top-none-mobile has-padding-bottom-none-mobile has-padding-left-none-mobile has-padding-right-none-mobile" action="javascript:">
                <div class="card-content">
                    <h1 class="title is-size-2 has-padding-left-none has-padding-right-none">Create profile to save progress</h1>
                    <p id="create-profile-explanation" class="is-size-6 has-padding-left-none has-padding-right-none"></p>
                    <div class="title is-size-5 has-margin-top-large has-margin-bottom-small">Email</div>
                    <input type="text" data-profile-property="email" name="email" class="input is-radiusless is-size-5 user-email" value="">
                    <p hidden="" data-label="emailIsInvalid" class="help is-danger is-size-7 has-margin-top-none">Invalid email address. Please try again.</p>
                    <div class="title is-size-5 has-margin-top-large has-margin-bottom-small">Display Name</div>
                    <input type="text" data-profile-property="displayName" name="display-name" class="input is-size-5" value="">
                    <p class="is-size-6 has-text-extra-subtle has-margin-top-none">Choose a display name with up to 50 characters</p>
                    <p hidden="" data-label="displayNameIsInvalid" class="help is-danger is-size-7 has-margin-top-none">Invalid DisplayName. DisplayName should not end with '.'.  It must be 2 to 50 characters in length.</p>
                    <div class="title is-size-5 has-margin-top-large has-margin-bottom-small">User Name and URL</div>
                    <div class="field is-horizontal">
						<div class="field-label is-normal is-side-by-side has-margin-bottom-small has-margin-right-small">
							<label class="label server-path has-text-weight-normal">https://techprofile.microsoft.com/</label>
						</div>
						<div class="field-body extend-input-field">
							<div class="field">
								<p class="control">
									<input type="text" data-profile-property="userName" name="user-name" class="input is-size-5">
								</p>
							</div>
						</div>
					</div>
                    <p hidden data-label="userNameExists" class="help is-danger is-size-7 has-margin-top-none">That username is unavailable. Please try another.</p>
                    <p hidden data-label="userNameIsReserved" class="help is-danger is-size-7 has-margin-top-none">That username is unavailable. Please try another.</p>
                    <p hidden data-label="userNameIsInvalid" class="help is-danger is-size-7 has-margin-top-none">Invalid UserName. UserName must start with a letter or number and can contain non consecutive dashes. It must be 3 to 40 characters in length.</p>
                    <div class="title is-size-5 has-margin-top-large has-margin-bottom-small">Country</div>
					<div id="create-country-list"></div>
                    <p id="create-optin-optout-privacy-policy" class="is-size-6 has-padding-left-none has-padding-right-none"></p>
                    <div id="create-opt-in-checkbox" class="has-margin-top-small"></div>
                    <nav class="level is-mobile has-margin-top-extra-large has-margin-bottom-none">
                        <div class="level-left">
                            <div class="level-item has-margin-none">
                                <button type="button" class="button is-dark title is-size-4 has-padding-left-extra-large has-padding-right-extra-large" id="cancel-register">Cancel</button>
                            </div>
                        </div>
                        <div class="level-right">
                            <div class="level-item has-margin-none">
                                <button class="button is-primary title is-size-4 has-padding-left-extra-large has-padding-right-extra-large" type="submit" name="register-button" data-bi-name="register">
                                    Register
                                </button>
                            </div>
                        </div>
                    </nav>
                    <p hidden data-label="alreadyRegistered" class="help is-danger is-size-7 has-margin-top-none is-flex has-flex-justify-content-end">You are already registered.</p>
                    <p hidden data-label="somethingWentWrong" class="help is-danger is-size-7 has-margin-top-none is-flex has-flex-justify-content-end">Something went wrong. Please try again later.</p>
                </div>
            </form>
        </div>
    </div>
</div>