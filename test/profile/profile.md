---
layout: ContentPage
page_type: profile
page_kind: detail
title: Profile
description: Profile
---
<div class="container">
    <div class="columns has-margin-none has-padding-top-extra-large-tablet">
        <div class="column is-3 has-padding-none-mobile has-padding-right-none-tablet">
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
                                <nav class="level is-hidden-tablet is-mobile has-margin-bottom-small">
                                    <div class="level-left">
                                        <div class="level-item has-margin-none">
                                            <div class="display-name" class="title is-size-3"></div>
                                        </div>
                                    </div>
                                    <div class="level-right">
                                        <div class="level-item has-margin-none">
                                            <div class="subtitle is-5 is-size-7">
                                                <a href="/edit" class="edit-link is-hidden" data-bi-name="edit"></a>
                                            </div>
                                        </div>
                                    </div>
                                </nav>
                                <div class="display-name title is-hidden-mobile is-size-3 has-text-centered has-text-wrap"></div>
                                <div class="user-name is-size-7 has-text-centered-tablet has-margin-none-mobile has-text-wrap"></div>
                                <div id="upn" class="is-size-7 has-text-centered-tablet has-margin-none-mobile is-hidden has-text-wrap" data-profile-property="upn"></div>
                                <div class="is-hidden microsoft-employee is-size-7 has-text-centered-tablet has-margin-none-mobile has-text-wrap">Microsoft Employee</div>
                                <div class="is-hidden-tablet subtitle is-5 has-margin-none-mobile has-padding-top-extra-small-mobile">
                                    <span class="member-since is-size-7 has-text-extra-subtle"></span>
                                </div>
                            </div>
                            <div class="columns is-hidden-mobile has-margin-top-extra-large has-margin-left-none has-margin-right-none has-margin-bottom-extra-small">
                                <div class="column is-9 has-margin-none has-padding-none has-text-left">
                                    <span class="member-since is-size-7 has-text-extra-subtle"></span>
                                </div>
                                <div class="column has-margin-none has-padding-none has-text-right">
                                    <a href="/edit" class="edit-link is-hidden" data-bi-name="edit"></a>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </form>
            <div id="report-abuse" class="has-padding-top-extra-small has-padding-bottom-medium has-padding-left-medium-mobile has-padding-right-medium-mobile is-text-primary">
                <a href="javascript:" data-bi-name="report-abuse">
                    <span class="docon docon-flag has-padding-right-extra-small" aria-hidden="true"></span>
                    <span class="title is-size-7 has-text-primary">Report Abuse</span>
                </a>
            </div>
        </div>
        <div class="column is-9 has-padding-left-large-desktop has-padding-none-mobile">
            <div hidden id="cvs-notification" role="alert" class="alert is-warning has-margin-top-none" aria-live="polite">
                <div class="level">
                    <div class="level-left has-flex-shrink">
                        <div class="level-item has-flex-shrink">
                            <span class="icon">
                                <span class="docon docon-status-error-outline" aria-hidden="true"></span>
                            </span>
                            <span id="cvs-notification-message" class="message"></span>
                        </div>
                    </div>
                    <div class="level-right">
                        <div class="level-item">
                            <button id="cvs-notification-dismiss" type="button" class="button is-text" aria-controls="cvs-notification">Dismiss</button>
                        </div>
                    </div>
                </div>
            </div>
            <div class="card">
                <div class="columns is-mobile has-margin-none has-padding-top-medium has-padding-bottom-medium has-padding-left-none-mobile has-padding-right-none-mobile">
                    <div class="column is-one-third has-text-centered has-margin-none has-padding-none">
                        <div><p class="title is-size-5">Level</p></div>
                        <div class="has-border-right-tablet"><p class="current-level title is-size-1"></p></div>
                        <div><p class="xp-point is-size-8 has-text-extra-subtle has-margin-none has-padding-none"></p></div>
                    </div>
                    <div class="column is-one-third has-text-centered has-margin-none has-padding-none">
                        <div><p class="title is-size-5">Badges earned</p></div>
                        <div class="has-border-right-tablet"><p class="badge-count title is-size-1"></p></div>
                    </div>
                    <div class="column is-one-third has-text-centered has-margin-none has-padding-none">
                        <div><p class="title is-size-5">Trophies earned</p></div>
                        <div><p class="trophy-count title is-size-1"></p></div>
                    </div>
                </div>
            </div>
            <div class="user-progress-section">
            </div>
            <div class="achievement-section">
            </div>
        </div>
    </div>
</div>