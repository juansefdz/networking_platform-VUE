<template>
  <div class="activity-timeline">
    <h2 class="timeline-title">Activity Timeline</h2>
    <ul class="timeline-list">
      <li class="timeline-item">
        <div class="timeline-icon invoice"></div>
        <div class="timeline-content">
          <h3>12 Invoices have been paid</h3>
          <p>Invoices have been paid to the company</p>
          <a href="/src/assets/data/ProfileZone/invoice.pdf" class="timeline-attachment">invoice.pdf</a>
          <span class="timeline-time">12 min ago</span>
        </div>
      </li>
      <li class="timeline-item">
        <div class="timeline-icon meeting"></div>
        <div class="timeline-content">
          <h3>Client Meeting</h3>
          <p>Project meeting with John @10:15am</p>
          <div class="timeline-client">
            <img src="/src/assets/images/user3.jpg" alt="Lester McCarthy" />
            <span>Lester McCarthy (Client)</span>
            <span>CEO of Pixinvent</span>
          </div>
          <span class="timeline-time">45 min ago</span>
        </div>
      </li>
      <li class="timeline-item">
        <div class="timeline-icon project"></div>
        <div class="timeline-content">
          <h3>Create a new project for client</h3>
          <p>6 team members in a project</p>
          <div class="timeline-team">
            <img src="/src/assets/images/user1.jpg" alt="Team member 1" />
            <img src="/src/assets/images/user2.jpg" alt="Team member 2" />
            <img src="/src/assets/images/user3.jpg" alt="Team member 3" />
            <img src="/src/assets/images/user4.jpg" alt="Team member 4" />
            <span class="team-more">+3</span>
          </div>
          <span class="timeline-time">2 Day Ago</span>
        </div>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: "ActivityTimeline",
  props: {
    activities: {
      type: Array,
      required: true,
    },
  },
};
</script>
<style scoped>
.activity-timeline {
  padding: 20px;
  background-color: #fff;
  border-radius: 10px;
}

.timeline-title {
  font-size: 24px;
  margin-bottom: 20px;
}

.timeline-list {
  list-style-type: none;
  padding: 0;
}

.timeline-item {
  display: flex;
  margin-bottom: 20px;
  position: relative;

  &:before {
    content: "";
    position: absolute;
    left: 15px;
    top: 30px;
    bottom: -30px;
    width: 2px;
    background-color: #e0e0e0;
  }

  &:last-child:before {
    display: none;
  }
}

.timeline-icon {
  width: 30px;
  height: 30px;
  border-radius: 50%;
  margin-right: 15px;
  flex-shrink: 0;

  &.invoice {
    background-color: #780B74;
  }
  &.meeting {
    background-color: #780B74;
  }
  &.project {
    background-color: #780B74;
  }
}

.timeline-content {
  flex-grow: 1;

  h3 {
    margin: 0 0 5px;
    font-size: 16px;
  }

  p {
    margin: 0 0 10px;
    color: #6e6b7b;
  }
}

.timeline-attachment {
  display: inline-block;
  padding: 5px 10px;
  background-color: #f8f8f8;
  border-radius: 4px;
  text-decoration: none;
  color: #333;
  font-size: 14px;
}

.timeline-client,
.timeline-team {
  display: flex;
  align-items: center;
  margin-top: 10px;

  img {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    margin-right: 10px;
  }
}

.timeline-team {
  img {
    margin-right: -10px;
    border: 2px solid #fff;
  }

  .team-more {
    background-color: #f8f8f8;
    border-radius: 50%;
    width: 30px;
    height: 30px;
    display: flex;
    align-items: center;
    justify-content: center;
    font-size: 12px;
  }
}

.timeline-time {
  font-size: 12px;
  color: #b9b9c3;
  display: block;
  margin-top: 5px;
}
</style>
