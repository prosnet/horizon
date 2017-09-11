<template>
    <aside class="main-sidebar">
        <ul class="nav">
            <router-link tag="li" to="/dashboard" active-class="nav-item-active" class="nav-item">
                <a class="nav-link">
                    <i>
                        <svg>
                            <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                 xlink:href="#zondicon-dashboard"></use>
                        </svg>
                    </i>
                    Dashboard
                </a>
            </router-link>

            <router-link tag="li" to="/monitoring" active-class="nav-item-active" class="nav-item">
                <a class="nav-link">
                    <i>
                        <svg>
                            <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                 xlink:href="#zondicon-search"></use>
                        </svg>
                    </i>
                    Monitoring
                </a>
            </router-link>

            <router-link tag="li" to="/metrics" active-class="nav-item-active" class="nav-item">
                <a href="#" class="nav-link">
                    <i>
                        <svg>
                            <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                 xlink:href="#zondicon-chart-bar"></use>
                        </svg>
                    </i>
                    Metrics
                </a>
            </router-link>

            <router-link tag="li" to="/recent-jobs" active-class="nav-item-active" class="nav-item">
                <a href="#" class="nav-link">
                    <i>
                        <svg>
                            <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                 xlink:href="#zondicon-cog"></use>
                        </svg>
                    </i>
                    Recent Jobs
                </a>
            </router-link>

            <router-link tag="li" to="/failed" active-class="nav-item-active" class="nav-item">
                <a href="#" class="nav-link">
                    <i>
                        <svg>
                            <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                 xlink:href="#zondicon-close-outline"></use>
                        </svg>
                    </i>
                    Failed
                </a>
            </router-link>

            <router-link tag="li" to="/settings" active-class="nav-item-active" class="nav-item">
                <div class="nav-item">
                    <a href="#" class="nav-link">
                        <i>
                            <svg>
                                <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                     xlink:href="#zondicon-wrench"></use>
                            </svg>
                        </i>
                        Settings
                    </a>
                </div>
            </router-link>

            <div class="nav-item">
                <a href="#" class="nav-link" onclick="event.preventDefault();
                                                        document.getElementById('logout-form').submit();">
                    <i>
                        <svg>
                            <use xmlns:xlink="http://www.w3.org/1999/xlink"
                                 xlink:href="#zondicon-close-solid"></use>
                        </svg>
                    </i>
                    Logout
                </a>
            </div>
        </ul>
    </aside>
</template>
