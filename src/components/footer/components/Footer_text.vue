<template>
  <span>
    <p>
      * The stated consumption and emissions values were determined in
      accordance with the legally stipulated measurement procedure. The WLTP
      test cycle completely replaced the NEDC test cycle with effect from 1
      January 2022. As a result, no NEDC values are available for vehicles with
      a type approval issued after this date.
    </p>
    <br />
    <p>
      The values do not refer to an individual vehicle and are not part of the
      offer; instead, they are solely for the purpose of comparing between
      different types of vehicles. Optional equipment and accessories
      (attachments, tyre formats etc.) may alter relevant vehicle parameters
      such as the weight, rolling resistance and aerodynamics and, alongside
      weather and traffic conditions and individual driving behaviour, may
      influence the fuel consumption, electricity consumption, CO2 emissions and
      performance values of a vehicle.
    </p>
    <br />
    <p>
      Due to the more realistic test conditions, fuel consumption and CO2
      emissions values will in many cases be higher in accordance with the WLTP
      than in accordance with the NEDC. There may have been corresponding
      changes to vehicle taxation since 1 September 2018 as a result of this.
      You can find further information on the differences between the WLTP and
      the NEDC at
      <a href="http://www.audi.co.uk/wltp">http://www.audi.co.uk/wltp.</a>
    </p>
    <br />
    <p>
      Further information on the official fuel consumption and the official,
      specific CO2 emissions of new passenger car models can be found in the
      “Guide on the fuel economy, CO2 emissions and power consumption of all new
      passenger car models”, available free of charge from all sales outlets and
      from DAT Deutsche Automobil Treuhand GmbH, Hellmuth-Hirth-Str. 1, 73760
      Ostfildern, Germany or at <a href="www.dat.de.">www.dat.de.</a>
    </p>
  </span>
</template>

<script>
export default {
  name: "Footer_text",
};
</script>

<style scoped>
@media (min-width: 0) {
  span {
    padding: 0 var(--rem);
  }
  a,
  p {
    font-size: 0.7rem;
    letter-spacing: 2px;
  }

  p {
    padding: 0 calc(var(--rem) * 1.8);
  }

  p:last-child {
    padding: 0 calc(var(--rem) * 1.8) 2rem;
  }

  a {
    color: inherit;
    transition: var(--transition);
  }

  a:hover {
    color: var(--dark-accent);
  }
}

@media (min-width: 1025px) {
  p,
  p:last-child {
    padding: 0;
  }
}
</style>
