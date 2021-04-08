<script>
	export let student;
	export let baseUrl;
</script>

<header>
    <div class="container">
        <div class="profile">
            <div class="profile-image">
                <img
                    src="{baseUrl}{student.Avatar.formats.thumbnail.url}"
                    alt=""
                />
            </div>
            <div class="profile-user-settings">
                <h1 class="profile-user-name">{student.Name}</h1>
                <button class="btn profile-edit-btn">Edit Profile</button>
                <button
                    class="btn profile-settings-btn"
                    aria-label="profile settings"
                >
                    <i class="fas fa-cog" aria-hidden="true" />
                </button>
            </div>
            <div class="profile-stats">
                <ul> 
                    <li><span class="profile-stat-count">{student.anecdotes.length}</span> Anecdotes</li>
                    <li><span class="profile-stat-count">{student.events.length}</span> Events </li>
                    <li><span class="profile-stat-count">{student.events.length}</span> Class Events </li>
                </ul>
            </div>
            <div class="profile-bio">
                <p>
                    {student.Description}
                </p>
            </div>
        </div>
        <!-- End of profile section -->
    </div>
    <!-- End of container -->
</header>
