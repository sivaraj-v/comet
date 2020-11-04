---
layout: ContentPage
page_type: profile
page_kind: edit
title: Edit Your Profile
description: Edit your profile
---
<div id="edit-profile-container" class="container">
    <div id="edit-profile" class="columns is-hidden has-margin-none has-padding-top-extra-large-tablet has-small-gaps">
        <div class="column is-3 has-padding-none-mobile">
            <form id="profile-section" class="card has-margin-none has-padding-none">
                <div class="columns has-margin-none is-mobile">
                    <div class="column is-3 is-hidden-tablet has-padding-left-medium">
                        <figure class="image is-96x96 is-center-aligned has-padding-top-none has-padding-bottom-none">
                            <img class="avatar-url has-background-grey-light is-rounded" aria-role="presentation" src="" aria-hidden="true">
                        </figure>
                    </div>
                    <div class="column has-padding-none">
                        <div class="card-content">
                            <figure class="image is-hidden-mobile is-112x112 is-center-aligned has-padding-top-none has-padding-bottom-none">
                                <img class="avatar-url has-background-grey-light is-rounded" aria-role="presentation" src="" aria-hidden="true">
                            </figure>
                            <div class="has-margin-top-large-tablet has-margin-top-medium-mobile has-padding-left-small-mobile">
                                <div class="title is-size-3 has-text-centered-tablet has-margin-bottom-small-mobile has-text-wrap" data-profile-property="displayName"></div>
                                <div class="is-size-7 has-text-centered-tablet has-margin-none-mobile has-text-wrap" data-profile-property="userName"></div>
                                <div id="upn" class="is-size-7 has-text-centered-tablet has-margin-none-mobile has-text-wrap" data-profile-property="upn"></div>
                                <div hidden class="is-size-7 has-text-centered-tablet has-margin-none-mobile has-text-wrap" data-profile-property="isMicrosoftUser">Microsoft Employee</div>
                                <div class="is-hidden-tablet subtitle is-5 is-size-7 has-margin-none-mobile has-padding-top-extra-small-mobile">
                                    <span class="is-size-7 has-text-extra-subtle">Member Since <span data-profile-property="createdOn"></span></span>
                                </div>
                            </div>
                            <div class="columns is-hidden-mobile has-margin-top-extra-large has-margin-left-none has-margin-right-none has-margin-bottom-extra-small">
                                <div class="column has-margin-none has-padding-none has-text-left">
                                    <span class="is-size-7 has-text-extra-subtle">Member Since <span data-profile-property="createdOn"></span></span>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </form>
        </div>
        <div class="column is-9 has-padding-none-mobile">
            <form id="edit-info-form" class="card has-padding-none" action="javascript:">
                <div class="card-content has-padding-top-extra-large-tablet has-padding-bottom-extra-large-tablet has-padding-left-extra-large-tablet has-padding-right-extra-large-tablet has-padding-top-medium-mobile has-padding-bottom-medium-mobile has-padding-left-medium-mobile has-padding-right-medium-mobile">
                    <h2 class="title is-size-3 has-margin-top-none has-margin-bottom-none">
                        Personal Info, Username and URL
                    </h2>
                    <div class="columns has-margin-none">
                        <div id="profile-update-avatar-section" hidden class="column is-3 has-padding-none has-margin-right-large-tablet">
                            <div class="has-margin-top-extra-large-tablet has-margin-top-large-mobile">
                                <figure class="image is-96x96 is-center-aligned has-padding-top-none has-padding-bottom-none">
                                    <img class="avatar-url has-background-grey-light is-rounded" aria-role="presentation" src="" aria-hidden="true">
                                </figure>
                                <button class="button is-12 is-fullwidth-mobile is-size-5 is-fullwidth" type="button" id="profile-update-avatar-button" name="profile-update-avatar-button">Change Picture</button>
                            </div>
                        </div>
                        <div class="column has-padding-none">
                            <div class="title is-size-6 has-margin-top-extra-large-tablet has-margin-top-large-mobile has-margin-bottom-medium">
                                <label for="user-name">User Name and URL</label>
                            </div>
                            <div class="field has-addons">
                                <p class="control">
                                    <a id="user-name-info" class="server-path button is-small is-text has-padding-left-none has-padding-right-extra-small has-text-subtle">https://techprofile.microsoft.com/</a>
                                </p>
                                <p class="control">
                                    <input type="text" data-profile-property="userName" id="user-name" name="user-name" class="input is-small" value="" aria-describedby="user-name-info" />
                                </p>
                            </div>
                            <p id="user-name-info" class="is-size-7 has-text-extra-subtle has-margin-top-none">Note: changing your username can have unintended side effects</p>
                            <p hidden data-label="userNameExists" class="help is-danger is-size-7 has-margin-top-none">That username is unavailable. Please try another.</p>
                            <p hidden data-label="userNameIsReserved" class="help is-danger is-size-7 has-margin-top-none">That username is unavailable. Please try another.</p>
                            <p hidden data-label="userNameIsInvalid" class="help is-danger is-size-7 has-margin-top-none">Invalid UserName. UserName must start with a letter or number and can contain non consecutive dashes. It must be 3 to 40 characters in length.</p>
                            <div class="title is-size-6 has-margin-top-extra-large-tablet has-margin-top-large-mobile has-margin-bottom-medium">
                                <label for="display-name">Display Name</label>
                            </div>
                            <input type="text" data-profile-property="displayName" id="display-name" name="display-name" class="input is-size-7" value="">
                            <p hidden data-label="displayNameIsInvalid" class="help is-danger is-size-7 has-margin-top-none">Invalid DisplayName. DisplayName should not end with '.'.  It must be 2 to 50 characters in length.</p>
                            <nav class="level has-margin-top-large has-margin-bottom-none">
                                <div class="level-left"></div>
                                <div class="level-right">
                                    <div class="level-item has-margin-none">
                                        <button type="submit" class="button is-12 is-primary is-fullwidth-mobile title is-size-5 has-padding-left-extra-large has-padding-right-extra-large" name="submit-button" data-bi-name="save">Save</button>
                                    </div>
                                </div>
                            </nav>
                            <p hidden data-label="saveSuccessful" class="help is-12 is-success is-size-7 has-margin-top-none is-flex has-flex-justify-content-end">Save successful.</p>
                            <p hidden data-label="somethingWentWrong" class="help is-12 is-danger is-size-7 has-margin-top-none is-flex has-flex-justify-content-end">Something went wrong. Please try again later.</p>
                        </div>
                    </div>
                </div>
            </form>
            <form id="download-data-form" class="card has-padding-none has-margin-top-large-tablet has-margin-none-mobile">
                <div class="card-content has-padding-top-extra-large-tablet has-padding-bottom-extra-large-tablet has-padding-left-extra-large-tablet has-padding-right-extra-large-tablet has-padding-top-medium-mobile has-padding-bottom-medium-mobile has-padding-left-medium-mobile has-padding-right-medium-mobile">
                    <h2 class="title is-size-3 has-margin-top-none has-margin-bottom-large">
                        Download Your data
                    </h2>
                    <p class="is-size-5">
                       This is where you can download a copy of your data.
                    </p>
                    <nav class="level has-margin-top-large">
                        <div class="level-left"></div>
                        <div class="level-right">
                            <div class="level-item has-margin-none">
                                <button type="button" id="download-data" class="button is-primary is-fullwidth-mobile title is-size-5 has-padding-left-extra-large has-padding-right-extra-large" data-bi-name="download">Download</button>
                            </div>
                        </div>
                    </nav>
                </div>
            </form>
            <form id="delete-profile-form" class="card has-padding-none has-margin-top-large-tablet has-margin-none-mobile">
                <div class="card-content has-padding-top-extra-large-tablet has-padding-bottom-extra-large-tablet has-padding-left-extra-large-tablet has-padding-right-extra-large-tablet has-padding-top-medium-mobile has-padding-bottom-medium-mobile has-padding-left-medium-mobile has-padding-right-medium-mobile">
                    <h2 class="title is-size-3 has-margin-top-none has-margin-bottom-large">
                        Delete Your Account
                    </h2>
                    <p class="is-size-5">
                        Deleting your information does not impact your Microsoft identity.
                    </p>
                    <nav class="level has-margin-top-large has-margin-bottom-none">
                        <div class="level-left"></div>
                        <div class="level-right">
                            <div class="level-item has-margin-none">
                                <button type="submit" class="button is-danger is-fullwidth-mobile title is-size-5 has-padding-left-extra-large has-padding-right-extra-large" data-bi-name="delete-account">Delete Account</button>
                            </div>
                        </div>
                    </nav>
                    <p hidden data-label="somethingWentWrong" class="help is-12 is-danger is-size-7 has-margin-top-none is-flex has-flex-justify-content-end">Something went wrong. Please try again later.</p>
                </div>
            </form>
        </div>
    </div>
</div>