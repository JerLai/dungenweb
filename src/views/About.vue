<template>
  <v-content class="about">
    <section id="the-dungen-project" style="padding: 0px 0px;">
      <h1 class="text-uppercase headline font-weight-bold mb-2 text-center">The DunGen Project</h1>
      <p class = "text-center mb-10">
        The DunGen Project was born out of a desire to combine several goals. Named "DunGen" to signify
        a dungeon generator, it was inspired by other dungeon generators out there made in the Unity Engine.
        The generator is a means to help with potential game development requiring procedural generation of
        dungeons, or to help in the hand-authoring of dungeons. This tool is planned to be an open tool for
        people without the explicit use of the Unity Engine for a variety of purposes.
      </p>
      <h1 class="text-uppercase headline font-weight-bold mb-2 text-center">Update Regarding stalled development "02/11/2025"</h1>
      <p class = "text-center mb-10">
        After the initial release of 1.0, I went ahead to research and learn more generation algorithms to implement.
        I wanted the next release to be more robust, to showcase more algorithms in order to fuel future development plans
        with games in Unity. However, after another 2 years of development, I decided to take a step back to rethink the whole tool.
        This is suppose to be a general purpose tool to help in creating map layouts for games that would want interesting dungeons
        generated on the fly or to be curated. Why am I trying to implement it in Unity? Would I not just be locked into using Unity for all future games?

        I took a while to ponder what I should do, whether I should keep using what I had or restart from scratch. It would be sad to throw away my current
        work but I had enough of working around Unity for something as simple as generating a grid layout that forms a map. I wanted to throw away some of
        extra features for something more streamlined first for the basic tool. Thus I decided to restart from scratch. However, algorithms and logic are easily
        migratable, just how it looks will be different. Coupled with the Unity fiasco towards its developers, it felt appropriate to do a refresh.

        Doing something like this alone with only your passion can be tricky, I respect all other developers that release something amazing. Going forward,
        I intend to incrementally make the tool as I intended: a simple tool for all that can be used to generate the layouts they desire.
      </p>
    </section>
    <section id="roadmap" style="padding: 0px 0px;">
      <h1 class="text-uppercase headline font-weight-bold mb-2 text-center">Future RoadMap</h1>
      <v-timeline>
        <v-timeline-item
          v-for="(goal, i) in goals"
          :key="i"
        >
          <v-card>
            <v-card-title>
              {{goal.name}}
            </v-card-title>
            <v-container>
              <v-row>
                <v-col cols="12" md="10">
                  {{goal.desc}}
                </v-col>
                <v-col
                  class="hidden-sm-and-down text-right"
                  md="2"
                >
                </v-col>
              </v-row>
            </v-container>
          </v-card>
        </v-timeline-item>
      </v-timeline>
    </section>
  </v-content>
</template>
<script>
export default {
    name: 'About',
    data() {
        return {
            goals: [
              {name: "DunGen UI", desc: "Tidying up the Unity UI in the demo, and for future versions for cleaner useability."},
              {name: "DunGen Builder 1.0", desc: "First full iteration of the procedural generator. Tidying up the Unity UI to provide cleaner intuition on how to use. Generate dungeons based on grid size, room size and more."},
              {name: "DunGen Builder 1.5", desc: "More algorithms implemented"},
              {name: "Personal Accounts", desc: "Account system to provide ways to share/save maps made."},
              {name: "DunGen Builder 2.0", desc: "Hand-author dungeons in a special mode. Draw your own rooms, hallways, and insert your own enemies, traps, treasures and events."},
              {name: "Scenario Blueprint 1.0", desc: "Simulation tool to create a dungeon blueprint for game scenarios, such as in Dungeons and Dragons"}
            ]
        }
    },
    mounted() {

    }
}
</script>
<style>
</style>
