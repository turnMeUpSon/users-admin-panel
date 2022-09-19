<script>
  import user1Pic from "../assets/images/image1.png";
  import user2Pic from "../assets/images/image2.png";
  import user3Pic from "../assets/images/image3.png";

  let users = [
    {
      id: 1,
      name: "Jan Miller",
      image: user1Pic,
      email: "jan@piedpiper.com",
    },
    {
      id: 2,
      name: "Maxim Krutonog",
      image: user2Pic,
      email: "max@piedpiper.com",
    },
    {
      id: 3,
      name: "Alexey krokhin",
      image: user3Pic,
      email: "alexkro@piedpiper.com",
    },
  ];

  const getUsers = () => {
    return users;
  };
</script>

<div>
  <h1>List of users</h1>
  {#each getUsers() as { image, name, email, id }, i (id)}
    <p>{i + 1}</p>
    <div>
      <img src={image} alt={name} />
      <p>{name}</p>
      <p>{email}</p>
    </div>
  {:else}
    <p>No user found.</p>
  {/each}
</div>
